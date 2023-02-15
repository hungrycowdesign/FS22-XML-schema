# FS22-XML-schema
A static source for XML and i3d schema used in Farming Simulator 22.  Reference these raw XSD files in your XML or i3d files to make your schema validation system agnostic.  For example, the standard root element of an i3d file looks like this:

'''xml
<?xml version="1.0" encoding="iso-8859-1"?>
<i3D name="armoirePallet" version="1.6" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://i3d.giants.ch/schema/i3d-1.6.xsd">
'''

Change the schema location URL to the i3d-1.6.xsd file in this repository, such that the root element now looks like this:

'''xml
<?xml version="1.0" encoding="iso-8859-1"?>
<i3D name="armoirePallet" version="1.6" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="https://raw.githubusercontent.com/hungrycowdesign/FS22-XML-schema/main/i3d-1.6.xsd">
'''

This will clear any warnings while viewing the i3d file in a text editor such as Visual Studio Code and the i3d file can now be validated against the schema using your tool of choice.
