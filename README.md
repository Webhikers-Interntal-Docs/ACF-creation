# ACF-creation

1. One page must have exactly one ACF Field Group

2. All fields on a page must be grouped into sections. A section is defined be the frontend. It starts and ends as soon you can identify a new section visually, **or** content-related.

5. A typical `homepage` could have the following setup for example:

![Section Groups](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/section-groups-en.png)

3. To group all fields into sections use the `group` field_type when you create a new advanced custom field.
4. ![Field Type Group](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/field-type-group.png)


5. Each field with the field_type `group` contains several fields. For eaxmple:

![Section Header Label](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/section-header-label.png)
![Section Header Fields](https://github.com/Webhikers-Interntal-Docs/ACF-creation/blob/main/section-header-fields.png)


6. If you see any kind of repetitive schema in the frontend, you always must use a field with the type `repeater`. Inside the repeater simply put the fields as you would do normally.

7. Please stick to our naming conventions as follows:

- Short Text Inputs: `Title`, `Subtitle` (If there is more than 2 short text inputs in 1 Group, you can give it a name of your choice)
- Long Text Inputs: `Description` (If there is more than 1 long text input in 1 Group, you can give it a name of your choice)
- Images: `Image` (If there is more than 1 image in 1 Group, you can give it a name of your choice)
- Background Images: `Background Image`.

