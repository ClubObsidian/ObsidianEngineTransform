# ObsidianEngineTransform
Uses javassist to transform classes on runtime by adding bindings to the classes you want to modify.

# Usage

    new TransformBuilder("oldClassToBindTo") //Old class that you want to bind to
    .redefineMethod("newClassToBindTo", "newMethodInNewClass", "oldMethodInOldClass") //new class, new method, old method in old class
    .build(); //redefineMethod can be called multiple times or you can build the class to update the class in the class path
    //Transformations should be done on module load
    //Mutator modules should depend on the module that has code that is to be mutated
    //Mutator modules should also depend on this module
    
# License

Transform is licensed under the MIT license.

Javassist is triple but for this project licensed under the Apache 2.0 license.
