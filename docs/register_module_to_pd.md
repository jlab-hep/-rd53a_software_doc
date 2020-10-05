# Register modules to the production DB

The functions to register modules in the production DB will be supported in LocalDB viewer. We are developing the function now for the next updates of LocalDB tools.<br>
So we need to register modules manually in the current situation.<br>
If you don't have an account for the production DB. Please sign up following the link below.<br>
Tutorial page for ITk production DB[(https://gitlab.cern.ch/jpearkes/itkpd_tutorial/blob/master/README.md)](https://gitlab.cern.ch/jpearkes/itkpd_tutorial/blob/master/README.md)<br>

Please execute the following commands in your shell.<br>

```bash
$ cd <YOUR_WORK DIRECTRY>
$ git clone https://gitlab.cern.ch/atlas-itk/sw/db/pixels/module-scaffolding-implementation.git
$ cd module-scaffolding-implementation/
$ source authenticate.sh
Input Access Code 1 for ITkPD: 
Input Access Code 2 for ITkPD: 
You have signed in as Hiroki  Okuyama. Your token expires in 7198s.
$ cd registerComponent/
```

Edit the file named module_registerCfg.json as below.<br>
```yml
{
  "project":"P",
  "subproject":"PG",
  "institution":"TITECH",
  "componentType":"MODULE",
  "type":"OUTER_SYSTEM_QUAD_MODULE",
  "properties":{
    "FECHIP_VERSION":"0",
    "ORIENTATION": true
  },
  "serialNumber":"20UPGM20000003",
  "child":{
    "BARE_MODULE":"20UPGB40500004",
    "PCB":"20UPGPQ0100003"
  }
}
```


The parameters in the file should be set according to the serial numbering scheme. 
The document is here. [Link](https://cds.cern.ch/record/2728364/)<br>
Details for each parameter are following.<br>
- "project": Input "P". "P" means "Pixel". You can always use it.<br>
- "subproject": Input a subproject according to the document.<br>
- "institution":Input your institution registered in the production DB.<br>
- "componentType": Input "module" when you register modules.<br>
- "type": Input a type of module you are registering in capital letter.<br>
- "properties": Input properties of the module according to the document.<br>
- "serialNumber": Input a serial number for the module according to the document.<br>
- "child": Input the PCB's and Bare module's serial number assembled in the module to link the id in the DB.<br><br>

After setting the config, run the command below to register the module in the production DB.
```bash
$ python3 registerQuadModule.py
```

<br>
You can check the registered module list in the page of the production DB below. You can go to the page by the following link.<br>
[https://itkpd-test.unicorncollege.cz/myComponents](https://itkpd-test.unicorncollege.cz/myComponents)

<br>
[&rarr; Back to the page](module_QC_flow.md)

