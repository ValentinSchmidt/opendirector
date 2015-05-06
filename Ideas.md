### simple IDE and plugins ###
start with a minimalistic IDE that only consist of the core components:
  * script editor
  * VM / interpreter / (bytecode) compiler
  * console/message window
  * debugger
Add a plugin/extension API, and have everything else (all multimedia authoring specific elements) as authoring plugins, maybe in the form of "wizzards" that output code and/or configuration text/xml files:
  * GUI builder/wysiwyg screen editor ("stage")
  * timeline/animation editor ("score")
  * asset manager ("cast")
  * ...

### reuse an existing VM and IDE ###
use an existing platform/VM and IDE, create an IDE extension/plugin that meets the demands of multimedia authoring

Possible Candidates:
  * Mono
    * Platform/VM: Mono CLI VM (CLR)
    * Extensions/Libraries: ?
    * GUI Builder: MonoDevelop GUI designer
    * IDE: MonoDevelop, Eclipse

  * HaXe/Neko
    * Platform/VM: NekoVM
    * Extensions/Libraries/APIs: SWHX, [HippoHX](http://hippohx.com/), AsWing
    * GUI Builder: AsWing GUIBuilder
    * IDE: FlashDevelop, Eclipse

  * Python
    * Platform/VM: Python VM
    * Extensions/Libraries: wxPython, PyGame, PythonCard, PyMedia
    * GUI Builder: wxGlade, [Boa Constructor](http://boa-constructor.sourceforge.net/), [VisualWx](http://visualwx.altervista.org/)
    * IDE: Boa Constructor, [(Open) Komodo Edit](http://en.wikipedia.org/wiki/Komodo_Edit#Komodo_Edit), Eclipse, [Aptana Studio Community Edition](http://en.wikipedia.org/wiki/Aptana)

  * Lua
    * Platform/VM: Lua VM
    * Extensions/Libraries/APIs: [LuaSDL](http://sourceforge.net/projects/luasdl/), [wxLua](http://wxlua.sourceforge.net/)
    * GUI Builder: [VisualWx](http://visualwx.altervista.org/)
    * IDE: Eclipse, [LunarEclipse](http://lunareclipse.sourceforge.net/), [LuaEclipse](http://luaeclipse.luaforge.net/)

  * XUL
    * Platform/VM: XULRunner
    * Extensions/Libraries: ?
    * GUI Builder: [EclipseXUL](http://eclipsexul.sourceforge.net/), [XulBooster](http://cms.xulbooster.org/)
    * IDE: Eclipse

  * (Chromeless) Browser
    * Platform/VM: Mozilla Prism, WebKit
    * Extensions/Libraries: existing (like Flash) or new scriptable NPAPI Browser Plugins
    * GUI Builder: ? (Nvu/Mozilla Composer)
    * IDE: Eclipse, Aptana, Nvu/Mozilla Composer

  * Java
    * Platform/VM: Java runtime (JRE), [Java Kernel](http://java.sun.com/developer/technicalArticles/javase/java6u10/)
    * Extensions/Libraries: JavaFX, AWT, Swing, OpenSwing, SWT, Eclipse Rich Client Platform (RCP)
    * GUI Builder: NetBeans GUI Builder (Matisse)
    * IDE: NetBeans IDE, Eclipse, custom Editor built with Open.XDEV Application Framework

### GUI Builder with abstract "regions" ###
have a GUI builder/form designer ("stage") that allows to define abstract "regions", independantly of specific widgets/media objects (like the 

&lt;region&gt;

 elements in the SMIL standard, or like director's sprites which allow exchanging the attached member)