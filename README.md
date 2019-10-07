<h3 align="center">
  Commands
</h3>
<p>
    json-server --watch db.json
<p>

<h3 align="center">
  Query Fragments
</h4>
<p>
<h5>Query name</h5>
  <pre>
    <code>
      query findCompany {
        company(id: "2") {
        name
        description
        users {
          id
          firstName
          age
          }
        }
      }
    </code>
  </pre>

<h5>Query name</h5>
  <pre>
    <code>
    {
      apple: company(id: "1") {
        id
        name
        description
      }
      google: company(id: "2") {
        id
        name
        description
      }
    }
    </code>
  </pre>



<h5>Query Fragment</h5>
  <pre>
    <code>
    {
      apple: company(id: "1") {
        ...companyDetails
      }
      google: company(id: "2") {
        ...companyDetails
      }
    }
    </code>
    <code>
    fragment companyDetails on Company {
      id
      name
      description
    }
    </code>
  </pre>
