# Making World-Ready Applications with the fcSDK

## Introduction to Internationalization and the fcSDK

The **fcSDK** is globally aware. It takes advantage of the comprehensive globalization/internationalization support in the Microsoft™ .NET Framework (for more information on the globalization and localization support in the .NET Framework, please read the guide 'Developing World-Ready Applications' in the .NET Framework SDK documentation). This allows the **fcSDK** to easily support multiple cultures and locales.

When developing world-ready applications, one of the primary concern that developers face is interpreting user input string/text data into strongly typed data types. This is especially important with number and date/time formats. A good guideline for developing a world-ready application is to handle these conversions and interpretations as soon as possible after the user has submitted the data. This usually means processing the conversion in the UI layer (web application or windows application) before passing the data further down into libraries and the data access layer.
 
The **fcSDK** follows this design guidelines and only takes strongly-typed data structures such as the .NET Framework intrinsic types "Int32", "DateTime", "Decimal", etc. It is the responsibility of the application using the **fcSDK** to handle the culturally-sensitive conversions of these values.

Since the **fcSDK** does not do any conversions of types from strings, there are no internationalization issues caused by the **fcSDK** itself in terms of storing or retrieving values to or from the database. Since the **fcSDK** works directly with the Clarify™ database and trusts that the data is consistent and culturally sensitive, it is possible that bad data in the database could be returned in a culturally insensitive way. If you input data into your database using means other than the **fcSDK**, you must be sure that these other means are doing so in a culturally-sensitive way.

## Using the fcSDK to help build world-ready applications

The **fcSDK** provides some convenience features and some customizability to assist you in developing world-ready applications.

* Persist the Culture Setting for each User's Session
		The ClarifySession object has a property, CurrentCulture, which allows you to store which culture the user selected to use for the current UI. The application using the **fcSDK** is required to manage this value. The **fcSDK** does not use this value for anything except when called through the Compatibility Layer. In this case, all strings passed in for number and date fields will be converted to real values according to the format of the culture specified by the CurrentCulture property.
* Customizing Exception Messages Thrown by the **fcSDK**
		By default, the **fcSDK** will throw U.S. English (en-US) error messages in the format of: "(errnum) Description" where errnum is the unique error number for this exception and description is an explanation of the reason the exception was thrown.

		These error messages can be customized by using the fc_string table. The **fcSDK** install guide details installing optional schema modifications. One of these involves adding a 'name' column to the fc_string table. If you apply this schema change, you can begin adding customized versions of error messages for individual cultures. You can customize the default en-US messages and/or add messages for other cultures as well. The **fcSDK** will attempt to load an error message for the user according to the setting of the CurrentCulture property on the Session. If an error message cannot be found for this locale and error number combination, an attempt will be made to load a custom en-US message. If no custom en-US message is found, then the default hard-coded en-US message will be used.

		Each error message has a unique error number and error string identifier such as 17248 and "FOUND_LOGIN_FROM_FCAPP_DISABLED". The fcSDK ships with a DAT file containing all the error messages. You can load all the messages or just the ones you wish to customize. Locate the one in the fc_string table you wish to modify and change the message as appropriate.

		Assuming the entire DAT file was loaded into the database, you can customize a particular message by issuing a simple SQL statement. For example, to customize error ID 17248:

		```
		update table_fc_string set string = 'My Custom Message', nstring = 'My 
		Custom Message' where id = 17248
		```

		Alternatively, you can edit the DAT file before importing and then import many changes at once.

		**NOTE:** The error message ID will always appear in the exception message. This cannot be customized or removed. This is to assist First Choice Support troubleshoot error messages which might be in languages other than English. Given the error number, the English message can be retrieved from the DAT file of all the error messages.

* Localizing Strings Using the StringCache
		If your database has the 'fc_strings' table loaded, you can use the [StringCache](/api/FChoice.Foundation.Clarify.StringCache.yml) class to access localized strings from this table. The fcSDK itself uses this table and the [StringCache](/api/FChoice.Foundation.Clarify.StringCache.yml) class to localize its own exception messages. If you do not have this table, the schema is located in the "fcflnet_schema.sch" file located in the "schema" folder in the fcSDK installation path.

		In order to start using [StringCache](/api/FChoice.Foundation.Clarify.StringCache.yml) to load localized messages, the fc_string schema must be added to your Clarify database instance.	Once the new schema is loaded, the localized strings can be entered or imported using normal Clarify tools (like dataex). Next, delete the fc_cache dir before restarting your application to ensure that the fcSDK will detect the new schema changes. When the application is restarted, the fcSDK will then automatically detect the presence of the fc_string table and cache the contents.

		**NOTE:** The fcSDK expects the format of the 'locale' field in the fc_string table to be XX_YY, xx_YY, or xx_yy where ''xx' is the two-letter ISO 639-1 country/regoincode2 of the country or region for which this string is intended and 'yy' is the two-letter code derived from the ISO 3166 specification. In cases where a two-letter language code is not available, the three-letter code derived from ISO 639-2 is used; for example, the three-letter code 'div' is used for cultures that use the Dhivehi language.  
		For more information on what are acceptable culture specifiers, please consult the .NET Framework SDK documentation on the CultureInfo class.

		Once the schema is properly loaded, the strings are entered, and the fcSDK has reloaded its cache, the strings can be accessed by using one of the overloads of the [FindFCString]() method on the [StringCache](/api/FChoice.Foundation.Clarify.StringCache.yml) object. These methods will attempt to locate the string with the specified ID or NAME for the specified culture. If none exists for that culture, it will try to locate the same string for culture 'en_US'. If none is found, it will finally try for culture 'en'. If no string was found in either the desired culture or in any of the fallback cultures, $$NULL$$ will be returned. The caller to this method must be prepared to deal with the possibility that a string may be missing. The fcSDK will log a warning when it cannot find a requested string to help track down missing string resources.