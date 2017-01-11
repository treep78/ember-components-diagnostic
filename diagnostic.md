# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    A profile on a company website. A person's personal info, image, summary, and the like could all be components. This is because they would be goot to have as templates that will not be linked to directly, but rather as a part of a view. This allows all profiles to use the same component templates.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    a component is generated with a template.hbs and component.js file. I beleive test files are also added and modified.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
      {{my-contact contact='contact'}}
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each my-contact.phoneNumber as |phoneNumber|}}
      {{my-contact/my-phone number='number'}}
    {{/each}}
    ```
