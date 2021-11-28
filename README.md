
## Detección de Hate Speech (HS)
**Paper**: "Exploring Hate Speech Detection in Multimodal Publications" Raul Gomez, Jaume Gibert, Lluis Gomez, Dimosthenis Karatzas in WACV 2020.
Más información en: https://gombru.github.io/2019/10/09/MMHS/

### Estructura del Repo

- `notebooks/*`
  En esta carpeta se encuentra un notebook por cada herramienta que hemos aprendido en el curso: Ray, Map Reduce, Spark, Modin y Dask. Con cada una de estas herramientas, hemos hecho la limpieza de los datos para que puedan ser usados para entrenar la LSTM con la cual detectaremos HS.

- `dataset/MMHS150K_GT.json`
	Diccionario de Python donde cada _key es el tweet ID_ y sus campos son:
	- `tweet_url`
	- `labels`: array con 3 labels numéricos [0-5]:
		- `0 - NotHate`
		- `1 - Racist`
		- `2 - Sexist`
		- `3 - Homophobe`
		- `4 - Religion`
		- `5 - OtherHate`
	- `img_url`
	- `tweet_text`: texto del tweet, **este campo tenemos que limpiar para dárselo al modelo LSTM**
	- `labels_str`: array con los 3 labels pero en versión texto


- `files/hatespeech_keywords.txt`
	Contiene los keywords que fueron usados para obtener los tweets.

- `files/train_ids.txt`
	`files/val_ids.txt`
	`files/test_ids.txt`
    Contiene los tweets IDs que se usaron en los 3 splits.

