# ACF-creation

## Contact Form Creation

1. When a website needs a contact form, please install [CF7 Plugin](https://de.wordpress.org/plugins/contact-form-7/).
2. Create a new form for each contact form you see in the frontend (mostly it's only one)
3. In the form, create a field for each form input you see in the frontend and give them descriptive names (the names can always be in english). Set required fields to required.
4. For each form create a field with the name `legal_check` as `text` and make it required.
5. In the email tab, apply your created fields to the email formatting (subject, from, to, message, tel, etc....)
6. Enter the `form_id` and all `fieldnames (inlcuding required:true/false` and `legal_check` of the form into the prject doc where you also enter the rest api endpoints of the pages you create.

## XD Export

**Please export ALL assets without any formatting or cropping (raw and original images and assets)**

## Example Tutorial for  Homepage Header

1. One page must have exactly one ACF Field Group

2. All fields on a page must be grouped into sections. A section is defined be the frontend. It starts and ends as soon you can identify a new section visually, **or** content-related.

3. A typical `homepage` could have the following setup for example:

![Section Groups](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/section-groups-en.png)

4. To group all fields into sections use the `group` field_type when you create a new advanced custom field.

![Field Type Group](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/field-type-group.png)

5. Each field with the field_type `group` contains several fields. For eaxmple:

`Section Header`

![Section Header Label](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/section-header-label.png)

Fields inside `Section Header`

![Section Header Fields](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/section-header-fields.png)

In reality, these fields would look like this in the frontend:

![Section Header Frontend](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/section-header-frontend.png)

It has a `title`, a `subtitle`, a `button` text and a list of `background_images` for the slider. You will find the naming conventions for the fields below.

6. If you see any kind of repetitive schema in the frontend, you always must use a field with the type `repeater`. Inside the repeater simply put the fields as you would do normally.

In `Section Header` -> `Background Images`

![Section Header Background Images](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/section-header-background-images.png)

In `Section Header` -> `Background Images` -> `Background_Image`

![Section Header Background Images Image](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/section-header-background-images-image.png)

## Naming Conventions

Please stick to our naming conventions as follows:

- Short Text Inputs: `Title`, `Subtitle` (If there is more than 2 short text inputs in 1 Group, you can give it a name of your choice)
- Long Text Inputs: `Description` (If there is more than 1 long text input in 1 Group, you can give it a name of your choice)
- Images: `Image` (If there is more than 1 image in 1 Group, you can give it a name of your choice)
- Background Images: `Background Image`.

## Input Types

**You only need to select the correct field type and you can leave all other field options default**

- Headlines and short sentences: input type - `Text`
- Descriptions and text with more than one row:
  - if the user needs the ability to format the text styling: input type - `Wysiwyg Editor`
  - if the user does not need the ability to format the text styling: input type - `Text Area`
- Images and Background Images: input type - `Image`
- Youtube Videos: input type - `Text` (Only Youtube ID)
- Google Maps: input type - `Text` (Only Map and coordinates ID)
- All Images MUST be arrays, not only image urls, so we can get more information about all images (additional info like width, or height, alt tags, etc...)

## Which content needs Advanced Custom Fields?

Basically, anything that is `content related` requires ACF. Anything that is `design related` does not require ACF.

### Example 1

![Wunschauto Benefits](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/wunschauto-benefits.png)

Here we need the following fields:

1. `title`
2. `subtitle`
3. `benefits` (must be a repeater)
    - `icon`
    - `title`
    - `description`

We do not want the user to enter 1, 2, 3, 4 for each benefit, since this can be done programmatically.

### Example 2

![Wunschauto Service](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/wunschauto-service.png)

Here we need the following fields:

1. `title`
2. `subtitle`
3. `description`
4. `services` (must be a repeater)
    - `title`
    - `subtitle`
    - `description`

We do not want the user to enter an image for the red label for each service item, since this can be done programmatically.


### Example 3

![Wunschauto Inseriert](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/wunschauto-inseriert.png)

Here we need the following fields:

1. `title`
2. `subtitle`
3. `services` (must be a repeater)
    - `title`

We do not want the user to enter an image for the red icon for each item, since this can be done programmatically.
