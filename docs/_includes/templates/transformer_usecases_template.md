
<div class="h3-box" markdown="1">

## {{include.title}}

{{include.description}}

**Input Annotator Types:** `{{include.input_anno}}`

**Output Annotator Type:** `{{include.output_anno}}`

{% if include.note %}

> **Note:** {{include.note}}

{% endif %}

{% if include.source_link %}

| **Python API:** {{include.python_api_link}} | **Scala API:** {{include.api_link}} | **Source:** {{include.source_link}} |

{% else %}

| **Python API:** {{include.python_api_link}} | **Scala API:** {{include.api_link}} |


{% endif %}

<details>

<summary class="button"><b>Show Examples</b></summary>

<div class="tabs-model-aproach" markdown="1">

{% include transformerUseCaseSelect.html %}

<div class="tabs-python-scala-box" markdown="1">

{% include programmingLanguageSelectScalaPython.html %}

This example shows how to predict classes by using the embeddings generated by the Transformer.

<div class="tabs-mfl-box" markdown="1">
```python
{{include.prediction_python_example}}
```
</div>

<div class="tabs-mfl-box" markdown="1">
```scala
{{include.prediction_scala_example}}
```
</div>

</div>

<div class="tabs-python-scala-box" markdown="1">

{% include programmingLanguageSelectScalaPython.html %}

This example shows how to train an Approach Annotator by using the embeddings generated by the Transformer.

<div class="tabs-mfl-box" markdown="1">
```python
{{include.training_python_example}}
```
</div>

<div class="tabs-mfl-box" markdown="1">
```scala
{{include.training_scala_example}}
```
</div>

</div>

<div class="tabs-python-scala-box" markdown="1">

{% include programmingLanguageSelectScalaPython.html %}

This example shows how to extract the embeddings generated by the Transformer.

<div class="tabs-mfl-box" markdown="1">
```python
{{include.embeddings_python_example}}
```
</div>

<div class="tabs-mfl-box" markdown="1">
```scala
{{include.embeddings_scala_example}}
```
</div>

</div>

</div>

</details>

</div>