<script>
  import { Switch, TextField, Chip, DataTable } from "./smelte";
  import data from "./data.json";

  let loading = false;
</script>
<!--
<style>
  main {
    font-family: sans-serif;
    text-align: center;
  }
</style>
-->

<main>
<b>Komponenty</b><br/>
  <Switch>aaa</Switch>
  <Chip>chips 1</Chip><Chip>chips 2</Chip>
 <!--
 -->
<br/>

<TextField label="Text field" outlined />
<TextField label="Number field" outlined type="number" min="10" max="100" />
<TextField label="Example Hint" outlined hint="Test hint" />
<TextField label="Validation Error example" outlined error="Test error" />
<TextField label="Text area field" textarea rows="5" outlined />
<!--
<DataTable
{loading}
data={[{}]}
    columns={[
      { label: "ID", field: "id", class: "md:w-10", },
      {
        label: "Ep.",
        value: (v) => `S${v.season}E${v.number}`,
        class: "md:w-10",
        editable: false,
      },
      { field: "name", class: "md:w-10" },
    ]}
 />
  
<div class="overflow-auto p-1">
  <DataTable
    {data}
    {loading}
    on:update={({ detail }) => {
      const { column, item, value } = detail;

      const index = data.findIndex(i => i.id === item.id);

      data[index][column.field] = value;
    }}
    columns={[
      { label: "ID", field: "id", class: "md:w-10", },
      {
        label: "Ep.",
        value: (v) => `S${v.season}E${v.number}`,
        class: "md:w-10",
        editable: false,
      },
      { field: "name", class: "md:w-10" },
      {
        field: "summary",
        textarea: true,
        value: v => v && v.summary ? v.summary : "",
        class: "text-sm text-gray-700 caption md:w-full sm:w-64"
      },
      {
        field: "thumbnail",
        value: (v) => v && v.image
          ? `<img src="${v.image.medium.replace("http", "https")}" height="70" alt="${v.name}">`
          : "",
        class: "w-48",
        sortable: false,
        editable: false,
      }
    ]}
  />
</div>
-->
</main>