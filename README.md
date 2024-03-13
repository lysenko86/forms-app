# Forms-App
Odore test task - create a structure without content (only folders and empty files) for 2 signup forms.

# Description
- Used stack: React, TypeScript, SCSS, Yup validator

- I have added root files (package.json and etc) just for better project view

- **folder "public"**
    - also for just for template

- **index.tsx**
    - main file, where we put root DIV element to DOM

- **index.module.scss**
    - common styles for whole project (styles for HTML, BODY, A, variables of colors, etc)

- each folder contains **index.ts** - it helps to import any file from anywhere with aliases and pretty short path

- since interfaces for props in components uses almost always only one time, I don't use names for them - { ... }: { ... }

- **src/components**
    - folder for smart and not reusable components (or pretty big components, or components of pages )
    - here we have App component with styles (it could be some app container), this App component should contain 2 forms

- **src/sharedComponents**
    - folder for smart reusable components (for example Form)

- **src/sharedComponents/Form**
    - this component will cover tag FORM, it will take 3 parameters: validationSchema, submitFunction and children

- **src/providers**
    - folder for api entities (for example - users), it should be able to send request and get response
    - requests data and responses data should be typified by types from **src/types** folder
    - also it should have standard object of response, for example: { data. status. msgError }

- **src/clients**
    - here we can have different APIs and therty part services
    - each "client" (for example apiClient) should be able to connect and work with some service

- **src/validationSchemas**
    - here we have different schemas for validation by Yup package

- **src/uiComponents**
    - folder for dumb components, very local and flexible components without access to outer states, or proviers - just for UI
    - each of them definetely reusable
    - Input, Button - we use them in both forms
    - Dropdown - it's for "gender" field
    - Checkbox - you can't signup without agreenment with policy
    - FormContainer - different layouts for fields, it has "children" parameter

- **src/svgComponents**
    - folder for icon-components, I like such using of SVG
    - this using helps us to change color or sizes just passing these parameters
