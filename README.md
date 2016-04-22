# OopFactory.X12
This is a copy of the project originally posted at https://x12parser.codeplex.com/

Their original readme at the time this copy was made:
Project Description
This is an open source .NET C# implementation of an X12 Parser.

The parser allows for a specification of any X12 transaction set to create a generic X12 xml representation of the hierarchical data contained within the X12 document.

No database integration is required by design, though  you can use the ImportX12 app to parse into a SQL Server database and skip the XML.

Motivation
The motivation for this project is to provide a quick and easy way to examine edi files without the overhead of creating databases as the target for parsed EDI files.

It aims to demystify the X12 standard and make parsing it accessible to the masses, not to just very expensive parsing tools.
It also aims to reduce the overhead of getting started with X12 parsing by not requiring any database integration to solve the problem of parsing the file.

Assumptions
The built-in specs contain all 4010 standards and some 5010 specifications, but you can inject your own if you are using a later standard or a non-public specification.

See Parsing an 837 Transaction to see an example of the three possible output formats and their corresponding code samples.

Contributor Blogs

Comparing Open Source EDI Software contributed by nth

Latest features:

Added SQL Server Database integration with the ImportX12 console app and SqlTransactionRepository class.
Added all 4010 specifications to Release 2.3.4.
Added ClaimParser application specific for 837 healthcare claim parsing to Release 2.2.4.
Adds the ability to unbundle an X12 file by a LoopID so that they can be processed individually. See Unbundling an X12 file by Loop ID for an example.
Adds ISpecificationFinder which allows the user to inject custom specifications. Derive the provided implementation SpecificationFinder to override only specific transactions. See Injecting your own X12 Specification
Unobtrusive X12 manipulation with the Interchange object. Examples of modifying an X12 document can be found in X12 Interchange Model.
Transformation to HTML to view X12 as X12 with translations as tool-tips in the example output below. See the last code sample in Parsing an 837 Transaction.
