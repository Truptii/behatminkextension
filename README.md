
# Behat Mink Extension

Mink Extension in Behat is used to automate acceptance scenarios for your website
This repository will help in setting up Behat with Mink Extension. 

Below are the steps to setup Behat with Mink Extension

1.Create your project folder
  ```
  mkdir projectfolder
  cd projectfolder  
```
2.Install composer 
  ``` curl -s https://getcomposer.org/installer | php ```

3.Require the dependancy for behat and drupal extension in your composer.json
```  

  "require": {
    "behat/mink-extension": "*",
},
  
```

4. Update the composer  ``` composer update ```

5. Proceed with behat installation by creating ```behat.yml``` file

6.Enable Mink Extension by adding the extension in behat.yml
 ```
 Behat\MinkExtension:
      base_url:  'Website URL '
      sessions:
        default:
          goutte: ~ 
 ```
 
7.Initialize Behat by executing the command ```bin/behat --init``` . This will create FeatureContext.php file and features folder.
In features folder you can create your own feature file to automation scripts using Gherkin. In FeatureContext.php you can create your
own step definitions using PHP

8.Execute command ```bin/behat -dl``` to view list of all steps (This is also to ensure that your behat setup is done properly)


  

