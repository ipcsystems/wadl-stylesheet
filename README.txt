wadl.xsl is an XSLT stylesheet for transforming WADL, a Web Application's XML-based interface specification, into human-readable HTML documentation.

It is available at https://github.com/ipcsystems/wadl-stylesheet.

-------------------------------------------------------------------------------
Usage

    You can use this with a transformation engine but most modern browsers can handle it. Simply add a processing directive to your XML
    
        <?xml version="1.0" encoding="UTF-8"?>
        <?xml-stylesheet type="text/xsl" href="wadl.xsl"?>
        <wadl:application xmlns:wadl="http://wadl.dev.java.net/2009/02"
            etc., etc.   
        </wadl:application>
        
    The stylsheet has been tested with IE 7, Firefox 4 and Chrome 10. Note that links for external XML schema types (http://www.w3.org/TR/xmlschema-2) do not work in Firefox 4. Also, IE and Chrome don't process the XSL if the wadl is opened locally through a file URL. Serve it up over HTTP.
    
    
    The stylesheet works with the current WADL W3C Submission (http://www.w3.org/Submission/wadl/) whose namespace is http://wadl.dev.java.net/2009/02. If you need it to work with the original namespace, http://research.sun.com/wadl/2006/10, simply change the stylesheet's document element's wadl namespace, as follows:
    
        <xsl:stylesheet 
         xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="2.0"
         xmlns:wadl="http://wadl.dev.java.net/2009/02"
         xmlns:xs="http://www.w3.org/2001/XMLSchema"
         xmlns:html="http://www.w3.org/1999/xhtml"
         xmlns="http://www.w3.org/1999/xhtml">
        ...
        </xsl:stylesheet>

      
-------------------------------------------------------------------------------
Limitations

    The stylesheet does not handle globally defined methods or representations. These must be embedded within method elements (embedded within resources/resource elements). Other limitations are noted in the file header.

-------------------------------------------------------------------------------
Examples

    The example.wadl is provided to show off the capabilities of the stylesheet.


-------------------------------------------------------------------------------
License

    Copyright (c) 2011 IPC Systems, Inc.
    
    Parts of this work are adapted from Mark Notingham's wadl_documentation.xsl, at
        https://github.com/mnot/wadl_stylesheets.
    
    This work is licensed under the Creative Commons Attribution-ShareAlike 3.0 License.
    To view a copy of this license, visit 
        http://creativecommons.org/licenses/by-sa/3.0/
    or send a letter to 
        Creative Commons
        543 Howard Street, 5th Floor
        San Francisco, California, 94105, USA


-------------------------------------------------------------------------------
Contact

    For questions, contact Mark Sawers <mark.sawers@ipc.com>.