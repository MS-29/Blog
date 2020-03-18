## Coral UI-3 based Granite UI Component

- Auto Complete Dialog Field

  > ```xml
  > <autoComplete
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/autocomplete"
  >   emptyText="Tag"
  >   fieldLabel="Tag Selector"
  >   multiple="{Boolean}false"
  >   name="./tag"
  >   required="{Boolean}true">
  >   <datasource jcr:primaryType="nt:unstructured"
  >     sling:resourceType="cq/gui/components/common/datasources/tags"
  >     namespaces="[workflow,we-retail]"/>
  >   <options jcr:primaryType="nt:unstructured"
  >     sling:resourceType="granite/ui/components/coral/foundation/form/autocomplete/list"/>
  > </autoComplete>

- Check Box Dialog Field

  > ```xml
  > <checkbox
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/checkbox"
  >   uncheckedValue="{Boolean}false"
  >   checked="{Boolean}true"
  >   value="{Boolean}true"
  >   text="Hide Section?"
  >   name="./hideSection"
  > />

- Field Set Dialog Field

  > ```xml
  > <fieldset jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/fieldset"
  >   jcr:title="User Information">
  >   <items jcr:primaryType="nt:unstructured">
  >     <firstName
  >       jcr:primaryType="nt:unstructured"
  >       sling:resourceType="granite/ui/components/coral/foundation/form/textfield"
  >       fieldLabel="First Name"
  >       name="./text"
  >       required="{Boolean}true"/>
  >     <lastName
  >       jcr:primaryType="nt:unstructured"
  >       sling:resourceType="granite/ui/components/coral/foundation/form/textfield"
  >       fieldLabel="Last Name"
  >       name="./text"
  >       required="{Boolean}true"/>
  >   </items>
  > </fieldset>

- Multi Field Dialog Field

  > ```xml
  > <multiField
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/multifield"
  >   fieldLabel="Emails"
  >   composite="{Boolean}true"
  >   required="{Boolean}true">
  >   <field jcr:primaryType="nt:unstructured"
  >     sling:resourceType = "granite/ui/components/coral/foundation/container"
  >     name="./emails">
  >     <items jcr:primaryType="nt:unstructured">
  >       <email jcr:primaryType="nt:unstructured"
  >         sling:resourceType = "granite/ui/components/coral/foundation/form/textfield"
  >         fieldLabel="Email"
  >         name="./email"/>
  >     </items>
  >   </field>
  > </multiField>

- Nested Check Box Dialog Field

  > ```xml
  > <nestescheckboxlist
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/nestedcheckboxlist"
  >   disconnected="{Boolean}false">
  >   <items jcr:primaryType="nt:unstructured">
  >     <asia jcr:primaryType="nt:unstructured"
  >       sling:resourceType="granite/ui/components/coral/foundation/form/checkbox"
  >       text="Asia"
  >       uncheckedValue="{Boolean}false"
  >       value="{Boolean}true"
  >       name="./asia">
  >       <sublist jcr:primaryType="nt:unstructured"
  >         sling:resourceType="granite/ui/components/coral/foundation/form/nestedcheckboxlist">
  >         <items jcr:primaryType="nt:unstructured">
  >           <bangladesh jcr:primaryType="nt:unstructured"
  >             sling:resourceType="granite/ui/components/coral/foundation/form/checkbox"
  >             text="Bangladesh"
  >             uncheckedValue="{Boolean}false"
  >             value="{Boolean}true"
  >             name="./bangladesh"/>
  >           <singapore jcr:primaryType="nt:unstructured"
  >             sling:resourceType="granite/ui/components/coral/foundation/form/checkbox"
  >             text="Singapore"
  >             uncheckedValue="{Boolean}false"
  >             value="{Boolean}true"
  >             name="./singapore"/>
  >         </items>
  >       </sublist>
  >     </asia>
  >     <europe jcr:primaryType="nt:unstructured"
  >       sling:resourceType="granite/ui/components/coral/foundation/form/checkbox"
  >       text="Europe"
  >       uncheckedValue="{Boolean}false"
  >       value="{Boolean}true"
  >       name="./europe">
  >       <sublist jcr:primaryType="nt:unstructured"
  >         sling:resourceType="granite/ui/components/coral/foundation/form/nestedcheckboxlist">
  >         <items jcr:primaryType="nt:unstructured">
  >           <spain jcr:primaryType="nt:unstructured"
  >             sling:resourceType="granite/ui/components/coral/foundation/form/checkbox"
  >             text="Spain"
  >             uncheckedValue="{Boolean}false"
  >             value="{Boolean}true"
  >             name="./spain"/>
  >           <germany jcr:primaryType="nt:unstructured"
  >             sling:resourceType="granite/ui/components/coral/foundation/form/checkbox"
  >             text="Germany"
  >             uncheckedValue="{Boolean}false"
  >             value="{Boolean}true"
  >             name="./germany"/>
  >         </items>
  >       </sublist>
  >     </europe>
  >   </items>
  > </nestescheckboxlist>

- Number Field Dialog Field

  > ```xml
  > <numberField 
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/numberfield"
  >   min="18"
  >   max="35"
  >   step="1"
  >   name="./age"
  >   value="28"
  >   fieldLabel="Age"
  >   required="{Boolean}true"
  > />

- Path Browser Dialog Field

  > ```xml
  > <pathBrowser
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/pathbrowser"
  >   fieldLabel="Link"
  >   name="./pathBrowser"
  >   rootPath="/content/"
  > />

- Radio Button Dialog Field

  > ```xml >}}
  > <radio
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/radiogroup"
  >   fieldLabel="Text Color"
  >   vertical="{Boolean}false"
  >   required="{Boolean}true"
  >   name="./color">
  >   <items jcr:primaryType="nt:unstructured">
  >     <primary jcr:primaryType="nt:unstructured"
  >       text="Primary"
  >       value="primary"/>
  >     <secondary jcr:primaryType="nt:unstructured"
  >       text="Secondary"
  >       value="secondary"/>
  >   </items>
  > </radio>

- Select List Dialog Field

  > ```xml
  > <select
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/select"
  >   fieldLabel="Continent"
  >   emptyText="Select a Continent"
  >   name="./select"
  >   required="{Boolean}true">
  >   <items jcr:primaryType="nt:unstructured">
  >     <asia jcr:primaryType="nt:unstructured"
  >       text="Asia"
  >       value="asia"/>
  >     <europe jcr:primaryType="nt:unstructured"
  >       selected="{Boolean}true"
  >       text="Europe"
  >       value="europe"/>
  >   </items>
  > </select>

- Swich Dialog Field

  > ```xml
  > <switch jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/switch"
  >   value="{Boolean}true"
  >   uncheckedValue="{Boolean}false"
  >   checked="{Boolean}true"
  >   fieldLabel="Watch Football?"
  >   name="./watchFootball"
  > />

- Tag Field Dialog Field

  > ```xml
  > <tagField
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="cq/gui/components/coral/common/form/tagfield"
  >   fieldLabel="Select Tags"
  >   name="./tagField"
  >   multiple="{Boolean}true"
  > />

- Text Field Dialog Field

  > ```xml
  > <textField
  >   jcr:primaryType="nt:unstructured"
  >   sling:resourceType="granite/ui/components/coral/foundation/form/textfield"
  >   fieldLabel="Text Field"
  >   name="./textField"
  >   required="{Boolean}true"
  > />
