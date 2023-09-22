# NHP Basal Ganglia taxonomy(CCN20230601)

Atlas of non-human primate basal ganglia, developed in collaboration with the BRAIN Initiative Cell Census Network (BICCN).

Steps for curation:

1- [Get Taxonomy Dvelopment Tools](#get-taxonomy-dvelopment-tools)
1- [Add your data](#add-your-data)
1- [Load your data](#load-your-data)
1- [Browse](#browse)

## Get Taxonomy Dvelopment Tools 

Pull the latest TDT docker image via following the steps defined in the project [GitHub Container Registry](https://github.com/brain-bican/taxonomy-development-tools/pkgs/container/taxonomy-development-tools). 

```
docker pull ghcr.io/brain-bican/taxonomy-development-tools:latest
```

## Add your data

Place your data (ex. [AIT115_annotation_sheet.tsv](https://github.com/brain-bican/taxonomy-development-tools/tree/main/examples/nhp_basal_ganglia/AIT115_annotation_sheet.tsv)) and configuration file (ex. [test_config.yaml](https://github.com/brain-bican/taxonomy-development-tools/tree/main/examples/nhp_basal_ganglia/test_config.yaml)) into your project's `input_data` folder.  

## Load your data

Run following command in your project root folder to ingest your data files:

```
bash ./run.sh make load_data
```

## Browse

Run following command in your project root folder to run the online data editor:
```
bash ./run.sh make serve
```

This command will print a set of logs including a log like `nanobot::serve: listening on 0.0.0.0:3000`. This means your web editor is ready, and you can start editing your data.

You can start browsing web taxonomy editor from: [http://localhost:3000/table](http://localhost:3000/table)

For further details see [Taxonomy Development Tools Documentation](https://brain-bican.github.io/taxonomy-development-tools/)