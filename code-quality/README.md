# Code Quality

## Formatting

### IDE Integration

#### IntelliJ IDEA

Import `formatter/intellij-java-dzp-style.xml` via _File -> Settings -> Editor -> Code Style -> Java -> Scheme -> Settings icon -> Import Scheme -> IntelliJ IDEA code style XML_ 

## Checkstyle

### IDE Integration

#### IntelliJ IDEA

Create a new configuration in _File -> Settings -> Other Settings -> Checkstyle_ and 
use the URL `https://raw.githubusercontent.com/dbmdz/development/master/code-quality/checkstyle.xml`. Also tick these settings as "active" and use them for 
"Only Java sources (including tests)".