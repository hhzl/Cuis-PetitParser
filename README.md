# Cuis-PetitParser #

PetitParser port to Cuis Smalltalk

Ported packages are:
* PetitParser-Core
* PetitParser-Parsers
* PetitParser-Tools
* PetitTests-Core
* PetitTests-Examples
* PetitTests-Tests

## Usage ##

Load packages into a Cuis image. It is assumed that the Cuis-PetitParser folder is a sibling of the Cuis folder


    | slash |
    slash _ FileDirectory slash.
    {
      '..', slash, 'Cuis-PetitParser', slash, 'PetitParser.pck' .
      '..', slash, 'Cuis-PetitParser', slash, 'PetitTests.pck' .
      '..', slash, 'Cuis-PetitParser', slash, 'PetitTutorial.pck'
    }
    do:
    [ :fileName | CodeFileBrowser installPackage:
                 (FileStream concreteStream readOnlyFileNamed: fileName)
    ]    



Then follow the tutorial in 
http://www.lukas-renggli.ch/blog/petitparser-1 and 
http://www.lukas-renggli.ch/blog/petitparser-2 .

The file PetitParserWorkspace.st can be opened in a workspace to follow tutorial instructions. 
The ExpressionGrammar and Evaluator described in tutorial part 2 are included in the additional package

* PetitTutorial

## References ##


 http://scg.unibe.ch/research/helvetia/petitparser

 http://www.lukas-renggli.ch/blog/petitparser-1

 http://www.lukas-renggli.ch/blog/petitparser-2

 Lukas Renggli. Dynamic Language Embedding With Homogeneous Tool
 Support. PhD thesis, University of Bern, October 2010.
 http://scg.unibe.ch/archive/phd/renggli-phd.pdf

 http://www.themoosebook.org/book/internals/petit-parser

 http://pharobooks.gforge.inria.fr/PharoByExampleTwo-Eng/latest/PetitParser.pdf