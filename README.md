# Çatalhöyük Image Metadata with AI

## Content

`catal_ai_labels.csv` contains predictions made with various methods about the content of images from the Çatalhöyük Archaeological Project. It also contains a selection of metadata from the original image repository. The following methods were used:

- The Clarifai Predict API
- Google Vision API (Labels only, not Entities)
- Google OCR (as part of the Google Vision API)
- Trained model on text detection ([model trained by Ch. Chute](https://github.com/chrischute/catal))
- Goole AutoML trained model

Out of a sample of 1000 images, Google labeled 962, out of those Clarifai labled 766. 

## Fields

### Identifiers

- **druid** - unique ID 
- **filename** 
- **purl** - link to the image viewer in the [Stanford Digital Repository](https://sdr.stanford.edu) - SDR)
- **thumbnail_url** - direct link to the thumbnail image in SDR 

### Predictions

- **label** 
- **label_score** 
- **predictor** Clarifai or Google
- **label_eval** manual review of label for correct/incorrect/undetermined
- **reviewer_notes** 
- **google_ocr** - either empty string or text (by Google)
- **text_embed_score** - score about how likely it is the image has embedded text
- **automl_label** 4 possible labels Find (Artifact), People_working, Burial, Architectural
- **automl_score** 

### Existing metadata

- **File_Description**
- **Keywords**
- **Feature.Type**
- **Find**
- **Site**
- **Building**
- **Unit**
- **Feature**
- **Space**
- **Area**
- **Mound**
- **Direction**
- **Photographer**
- **Associated.Building**
- **Associated.Space**
- **Associated.Feature**
- **View**
- **Lab.Record.ID**
- **Lab.Team**
- **Year**
- **Rating**
