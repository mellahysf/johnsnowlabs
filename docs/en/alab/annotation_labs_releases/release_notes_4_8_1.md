---
layout: docs
header: true
seotitle: Annotation Lab | John Snow Labs
title: Annotation Lab Release Notes 4.8.1
permalink: /docs/en/alab/annotation_labs_releases/release_notes_4_8_1
key: docs-licensed-release-notes
modify_date: 2023-03-23
show_nav: true
sidebar:
  nav: annotation-lab
---

<div class="h3-box" markdown="1">

## 4.8.1

Release date: **22-03-2023**

## More Powerful Prompts, New Annotation Gesture, and Enhanced Support for Floating Licences in NLP Lab 4.8

NLP Lab 4.8 brings more power to the prompts allowing a more efficient text preannotation, it adapts to the user’s preferences in terms of annotation gestures, adds supports for bundles of floating licenses shared across the annotation team for parallel preannotation, training, and experiments in the playground. It also includes a long list of optimizations covering project configuration steps, large projects export, or automatic download of missing resources.  Here are the highlights of this release:

## More Powerful Prompts

NLP Lab 4.8 introduces several new features that enhance prompt-based
preannotation. One significant improvement is the incorporation of
negative questions into prompt definitions, which allows users to
establish characteristics that do not apply to the target entity or
relation. This version also enables the creation of relation prompts
using labels from custom models even if trained with different
embeddings, providing more flexibility for prompt-based preannotation.
Additionally, the software now automatically downloads prompt
dependencies and supports prompt import/export. The prompt definition
page also features a dynamic question count and filters for easy
navigation.

### Combining Positive and Negative Questions for More Precise Prompts Definition

NLP Lab 4.8 enhances the precision of entity annotation using prompts
by incorporating negative questions. On the prompt definition screen,
users can now specify two categories of questions - *Questions that
establish the characteristics of* *the target entity* and *Questions
that establish the characteristics that do not apply to* *the entity*.
Both the affirmative and negative definitions will be executed as
separate prompts, integrated into the same pipeline, enabling users to
eliminate incorrect entities generated by the prompts. This feature will
substantially boost the efficiency of prompt-based entity generation and
streamline the process for our users.

![Screen Recording 2023-03-21 at 2 29 05 PM](https://user-images.githubusercontent.com/17021686/226559658-425fee52-1856-4ad2-bf9e-b64092b0e9ef.gif)

### Relation Prompts Combine Entities from Models Trained with Different Embeddings 

NLP Lab allows the definition of relation prompts by combining entities
defined in pre-trained models, rules, and prompts. However, previous
versions of the software did not allow users to create relation prompts
using custom-trained models. In this update, users can implement and use
relation prompts linking 2 entities defined in custom-trained models
(e.g. trained via the NLP Lab). Moreover, there is no restriction for
the reference models which can also be trained using different
embeddings. We are confident that this new feature will enhance the
power of the prompts and offer more flexibility for prompt-based
preannotation.

### Automatically Download Necessary Prompt Dependencies

NLP Lab Prompts are created based on Zero Shot models. The later are
part of the Healthcare, Finance and Legal libraries and are accessible
only in the presence of a valid license key. The prompt definition
options are populated according to license availability: e.g. if a
Healthcare NLP license is available, the Healthcare option will be
active in the Domain dropdown. As such, when creating a prompt, the user has
to choose the domain of the prompt, and based on that, NLP Lab will
infer the Zero Shot model needed by the prompt.

When users select one of the active domains if the corresponding Zero
Shot model is not available locally, NLP Lab will automatically download
it from the NLP Models Hub.

![Screen Recording 2023-03-20 at 2 23 41 PM](https://user-images.githubusercontent.com/17021686/226288623-5e1ca39b-b6ce-4fdc-b058-b290e6765ede.gif)

### Import/Export Prompts

Prompts are preannotation resources that users often want to move from
one instance of the NLP Lab to another or to archive for future
reference. NLP Lab now supports prompt import and export from the UI.
The user can import a ZIP/JSON file containing one or several prompt
definitions. The imported prompts will become available on the Prompts
page under the Hub menu item.

Users can also export prompts in JSON format via the burger menu
available for each prompt.
![Screen Recording 2023-03-20 at 2 38 56 PM](https://user-images.githubusercontent.com/17021686/226291321-1bd5164a-c9e8-459b-a5a4-bbbc2591c54a.gif)


### Dynamic Count of Questions on the Prompt Definition Page

Each prompt can include a maximum of 30 positive questions and 30 negative
questions. For facilitating user actions when defining/updating prompts,
NLP Lab now includes a count of the number of questions added so far.
For instance, if two questions have been added while creating a prompt,
then the UI should show **Questions(2/30)**
![Screen Shot 2023-02-22 at 2 02 42 PM](https://user-images.githubusercontent.com/17021686/226298895-bc06c68e-e9d4-40ce-897a-511731be7a42.png)

### Filters in the prompt page

The Prompts page can become crowded very quickly as prompts are quite
popular and easy to define and use for preannotation, especially by non
technical users. For helping users quickly identify the prompts they
need, a search option is available as well as 2 filters. Using the 2
dropdown menus at the top right side of the page, prompts can be
filtered based on their Type or Domain.
![Screen Recording 2023-03-20 at 3 02 44 PM](https://user-images.githubusercontent.com/17021686/226298234-fb3ce678-4107-4dfb-8483-7af4c01b89e4.gif)

## Undo Changes For Prompt and Rules in the playground

We are thrilled to introduce the Undo feature added to the NLP Lab
Playground. This function enables users to quickly undo any changes made
during their current experimental session. By selecting the \"Undo
Changes\" button, all modifications made to the prompt/rules will be
reverted to their original state. We are confident that this feature
will significantly improve the user experience by providing greater
control over the editing process.


## New Annotation Gesture

Some of our users suggested updating the annotation gesture we
initially offered, as it was counter-intuitive, especially for users
accustomed to modern text editing tools. Specifically, the process of
first selecting the Label and then selecting the chunk to annotate may
not feel natural anymore, as tools such as MS Word, where you first
select a text and then have options to format or access contextual menus
that open next to your selection, have changed the way we all feel about
text manipulation. We hear you!

To make NLP Lab more intuitive and user-friendly, NLP Lab now supports a
new way of annotating text. This new feature allows users to select the
text first and then choose the label to apply. We believe that this will
make the annotation process more intuitive and efficient for many users.

This feature is available for both text projects and Visual NER
projects. You are now able to switch between the two options: selecting
text and assigning an entity, or selecting an entity and assigning text.
Both will work. This way, users can choose the annotation method that
works best for their project and their personal preferences.
![annotategesture](https://user-images.githubusercontent.com/33893292/226648116-217fc48e-a333-402c-b857-1e99915a7a9b.gif)



## Optimized Project Configurations

### Automatic Model Download During Project Import

When a user imports a project in NLP Lab 4.8, the system automatically
downloads any absent models utilized by the imported project. To enable
users to check whether the models have been downloaded or not, a new
section named \"Download Models\" has been included in the Import
status. If the required models have been downloaded or are already
present, a green tick will be displayed. On the other hand, if the
download process is unsuccessful, a red cross will be shown.

![Screen Shot 2023-03-20 at 3 32 11 PM](https://user-images.githubusercontent.com/17021686/226304501-1b96da3f-a998-4eda-a60d-2abad3aac144.png)

When the automatic download of a model/embeddings fails, an error
message is displayed on the model card in the Hub-\>Models page. Users
can hover over the question mark icon to see the details.

![Screen Shot 2023-03-20 at 3 41 59 PM](https://user-images.githubusercontent.com/17021686/226306376-68a66fa7-0096-457d-9195-229ea7548f4a.png)

### Update the behavior of the save button on the Project configuration page

While setting up the configuration, the user can now choose to save the
settings on all configuration sections without being redirected to
another page or having to deploy a preannotation server. After saving
the configuration, the user can deploy the pre-annotation server by
pressing the Pre-Annotate button from the tasks page or navigating to
the Configuration -\> Customize Labels page and save the configuration
there. Once the server is deployed, the user will either be directed to
the Tasks page or to the Import page.

### Missing Embeddings Warning in the Configuration Page

If embeddings are missing for a model that is part of a project
configuration, a black warning message was displayed on the
configuration page to alert the user. This warning message was not
visible before, but now the displayed text ensures that the user can see
the error.
![Screen Shot 2023-03-20 at 3 58 43 PM](https://user-images.githubusercontent.com/17021686/226310272-b97051e9-5c6f-411b-8964-0cd7f2fbcee4.png)

### Efficient Export for Large Projects

Visual NER projects, pre-annotations, and training have substantially
increased NLP Lab project sizes. Unfortunately, this growth has made
importing and exporting tasks or projects time-consuming, especially
when dealing with large files. The new version of the system has
addressed this issue by enhancing both project and task exports, making
it possible to quickly export large files and manage a vast number of
tasks. This optimization also applies to text-based projects, where the
export time has been reduced by a factor of ten.


The current version of the system includes a pop-up message that appears
before exporting both tasks and projects. This message notifies the user
that the system is preparing the data for download and advises them to
remain on the page and avoid enabling pop-ups to prevent any
interruptions. Once the data preparation is complete, the download will
start automatically, and the user will not need to take any additional
steps.

<img width="1480" alt="Screenshot 2023-03-19 at 12 24 03 PM" src="https://user-images.githubusercontent.com/33893292/226158618-0433e661-19da-4785-a723-809335c159ba.png">

## Enhanced Support for Floating Licenses 

### Support for Bundles of Licenses 

We are delighted to inform you that NLP Lab now offers support for
bundles of floating licenses. Those are licenses that enable multiple
pre-annotation/training servers to run concurrently based on the values
of the \"max_parallel_jobs\" parameter. In the previous version, our
floating license system only allowed for one pre-annotation/training
server to operate at a time. With this new update, users can enjoy the
benefits of a single floating license that can support multiple
pre-annotation/training servers simultaneously.

![new_floating-license](https://user-images.githubusercontent.com/10557387/226275799-271aff30-3d8e-4465-860b-45c2c613298a.gif)

### Display a banner showing the number of days remaining for the available trial license

NLP Lab improves the user experience by providing more accessible
information about license validity. Currently, users can only check
their license status on the Licenses page, which may not be convenient
as it requires manual action. To address this issue, we have added a new
feature that displays a warning on the user interface before the license
expires. This notification reminds you to review your subscription
status or renew your license before it expires. For trial licenses with
less than 30 days remaining, a banner will be displayed on the UI
indicating the remaining trial days and a link to create a new
subscription. This way, you can easily keep track of your trial period
and take the necessary steps before it ends.

<img width="1264" alt="Screenshot 2023-03-15 at 9 53 36 PM" src="https://user-images.githubusercontent.com/33893292/226554074-90dcc235-6b5b-4fbc-870f-28db4c387af7.png">

## Improvements

### Increased Flexibility in Username Definition 
With the latest release of NLP Lab, users can create usernames with increased flexibility and ease.
Specifically, support has been added for the use of the underscore
symbol \"\" in usernames. This enhancement will enable users to create
unique and more expressive usernames that better represent their
identity or brand. Furthermore, this feature will allow users to avoid
any potential conflicts or duplications with other usernames.

### Improved User Experience with Clearer Relation Prompts

NLP Lab has recently introduced an improvement to the way relation
prompts are displayed in the Pre-annotation pop-up. Previously, the
relation prompts were shown under the generic \"Pre-annotation prompts\"
category, which may have caused confusion for users. With this update,
relation prompts are now shown under a separate sub-heading of \"RE
prompts\" or \"Relation prompts,\" providing clearer and more organized
categorization. This improvement will enable users to manage the
creation and deployment of relation prompts more intuitively and
efficiently.

### Enhanced Accessibility and Functionality of Model Hub Page

To improve the accessibility and functionality of the Model Hub page,
NLP Lab has implemented several changes in its latest version. One such
improvement is the ability to distinguish between downloadable models
and license-restricted models. Models that require a license will now be
disabled when the appropriate license is not available, making it easier
for users to navigate and select models to reuse. Another enhancement is
the introduction of a new menu on the model/rules card, which allows
users to effortlessly download models from Modelshub or open them in the
playground. This menu provides a more streamlined and convenient way for
users to access and utilize the available models and resources.

</div><div class="prev_ver h3-box" markdown="1">

## Versions

</div>

{%- include docs-annotation-pagination.html -%}