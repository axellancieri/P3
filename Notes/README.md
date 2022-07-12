<!-- # P3 -->
 <!-- Treehouse FEWD project 3 -->
<!--TABLES EXAMPLE -->
 <table>
      <caption>Employee Information</caption>
      <thead>
        <tr>
          <th scope="col">Name</th>
          <th scope="col">E-mail</th>
          <th scope="col">Job role</th>
        </tr>
      </thead>
      <tfoot>
        <tr>
          <td colspan="3">Data is updated every 15 minutes.</td>  
        </tr>  
      </tfoot>
      <tbody>
        <tr>
          <th scope="row">Nick Pettit</th>
          <td>nick@example.com</td>
          <td>Web Designer</td>
        </tr>
        <tr>
          <th scope="row">Andrew Chalkley</th>
          <td>andrew@example.com</td>
          <td>Front-End Developer</td>
        </tr>
        <tr>
          <th scope="row">Dave McFarland</th>
          <td>dave@example.com</td>
          <td>Front-End Developer</td>
        </tr>
        <tr>
          <th scope="row">Guil Hernandez</th>
          <td>guil@example.com</td>
          <td>Web Designer</td>
        </tr>
      </tbody>
    </table>
<!-- FORM -->
      <form action="index.html" method="post">
        
<h1>Sign Up</h1>

<fieldset>
  
  <legend><span class="number">1</span> Your basic info</legend>
  <!-- INPUT -->
  <label for="name">Name:</label>
  <input type="text" id="name" name="user_name">

  <label for="mail">E-mail:</label>
  <input type="email" id="mail" name="user_email">

  <label for="password">Password:</label>
  <input type="password" id="password" name="user_password">
  <!-- INPUT RADIO -->
  <label>Age:</label>
  <input type="radio" id="under_13" value="under_13" name="user_age"><label for="under_13" class="light">Under 13</label><br>
  <input type="radio" id="over_13" value="over_13" name="user_age"><label for="over_13" class="light">13 or Older</label>
  
</fieldset>

<fieldset>
  
  <legend><span class="number">2</span> Your profile</legend>

  <label for="bio">Biography:</label>
  <textarea id="bio" name="user_bio"></textarea>
<!-- SELECT - OPTION -->
  <label for="job">Job role:</label>
  <select id="job" name="user_job">
    <optgroup label="Web">
      <option value="frontend_developer">Front-End Developer</option>
      <option value="php_developer">PHP-End Developer</option>
      <option value="python_developer">Python-End Developer</option>
      <option value="rails_developer">Front-End Developer</option>
      <option value="web_designer">Web Designer</option>
      <option value="wordpress_developer">WordPress Developer</option>
    </optgroup>
      <optgroup label="Mobile">
    <option value="android_developer">Android Developer</option>
    <option value="ios_developer">iOS Developer</option>
    <option value="mobile_developer">Mobile Developer</option>
        </optgroup>
    <optgroup label="Business">
    <option value="business_owner">Business Owner</option>
    <option value="freelancer_developer">Freelancer</option>
    </optgroup>
  </select>
    <!-- CHECKBOX -->
  <label>Interests:</label>
  <input type="checkbox" id="development" value="interest_development" name="user_interest"><label class="light" for="development">Development</label><br>
  <input type="checkbox" id="design" value="interest_design" name="user_interest"><label class="light" for="design">Design</label><br>
  <input type="checkbox" id="business" value="interest_business" name="user_interest"><label class="light" for="business">Business</label><br>
  
  </fieldset>

<button type="submit">Sign Up</button>

</form>