 <h2>Quick Start</h2>
          <p>
            If you reading this - you probably wanted pagination for your bot,
            don't worry, we gotchu!
          </p>
          <p>install spud.js (click on codeblock to copy)</p>
          <pre
            class="prettyprint"
            onclick="copyText(this)"
          ><code>npm i spud.js@latest</code></pre>
          <p>Import spud.js into your project</p>
          <pre
            class="prettyprint"
            onclick="copyText(this)"
          ><code class="language-javascript">const { ButtonPaginationBuilder, MenuPaginationBuilder } = require('spud.js');</code></pre>
          <p>Afterwards, we can create a quite simple example pagination</p>
          <h4>Button Pagination</h4>
          <p>
            In button pagination builder, only message/interaction, and embeds
            are required on a pagination. you can add embeds using
            <a
              href="https://github.com/MrPotato30/spudjs-docs/tree/main/docs/packages/ButtonPaginationBuilder#addembedsembeds"
              ><code class="inline-codeblock">.addEmbeds(...)</code></a
            >. You can also set embeds in button pagination builder using
            <a
              href="https://github.com/MrPotato30/spudjs-docs/tree/main/docs/packages/ButtonPaginationBuilder#setembedsembeds"
              ><code class="inline-codeblock">.setEmbeds(...)</code></a
            >
            as you can see from the code example below.
          </p>
          <pre
            class="prettyprint"
            onclick="copyText(this)"
          ><code class="language-javascript">const page1 = new MessageEmbed().setDescription("This is page 1");
const page2 = new MessageEmbed().setDescription("This is page 2");

const pagination = new ButtonPaginationBuilder(message)
  .setEmbeds(page1, page2);

pagination.send();</code></pre>
          <div class="devider"></div>
          <br />
          <h4>Menu Pagination</h4>
          <p>
            In menu pagination builder however, message/interaction, embeds, and
            labels are required.<br />you have to set the embed with the label
            in an options object. add options object with
            <a
              href="https://github.com/MrPotato30/spudjs-docs/tree/main/docs/packages/MenuPaginationBuilder#addoptionsdata"
              ><code class="inline-codeblock">.addOptions(...)</code></a
            >
            or set pagination options with
            <a
              href="https://github.com/MrPotato30/spudjs-docs/tree/main/docs/packages/MenuPaginationBuilder#setoptionsdata"
              ><code class="inline-codeblock">.setOptions(...)</code></a
            >
            as you can see from the example below.
          </p>
          <pre
            class="prettyprint"
            onclick="copyText(this)"
          ><code class="language-javascript">const pagination = new MenuPaginationBuilder(message).setOptions( 
  { embed: page1, label: "Page 1" },
  { embed: page2, label: "Page 2" }, 
  { embed: page3, label: "Page 3" } 
);

pagination.send();</code></pre>
          <p>
            These are the previews of the button pagination and menu pagination
            examples created with the code above.
          </p>
          <img
            src="https://media.discordapp.net/attachments/825656508464758809/1048945045325221908/brave_HyldTaWVJ3.png"
            alt="preview"
            class="preview"
          />
          <img
            src="https://media.discordapp.net/attachments/825656508464758809/1049880649223385179/brave_CdPFwVkTAN.png"
            alt="preview"
            class="preview"
          />
          <p>Easy as that.</p>
          <div class="devider"></div>
          <p>
            Now that we've seen some starter code for button and menu pagination
            in Spud.js, let's try out some examples of customizing these
            pagination builders. Both the button and menu pagination builders
            have some customization options in common, so we will cover those
            first.
          </p>
          <ul>
            <li>
              <code class="inline-codeblock">time</code> - This is the length of
              time in milliseconds that users are allowed to interact with the
              pagination. This specifies how long the pagination will remain
              active before it automatically ends. If not specified, the
              pagination will remain active until the bot restarts.
            </li>
            <br />
            <li>
              <code class="inline-codeblock">max</code> - This is the maximum
              amount of time users are allowed to interact with the pagination
              so that users cannot keep interacting with the pagination open
              indefinitely.
            </li>
            <br />
            <li>
              <code class="inline-codeblock">filter</code> - This is the filter
              that determines which user are allowed to interact with the
              pagination. This allows only the user to control the interaction
              and prevent unwanted behavior on the pagination. If not specified,
              the user in message.author can only use the pagination.
            </li>
            <br />
            <li>
              <code class="inline-codeblock">idle</code> - Accepts a boolean
              value that determines whether the time interval for the pagination
              should be reset on every user interaction. If set to true, the
              pagination will remain open as long as there is continuous user
              interaction.
            </li>
            <br />
            <li>
              <code class="inline-codeblock">content</code> - This is a string
              value that specifies the message content to be shown in the
              pagination. It will be displayed outside pagination embeds.
            </li>
          </ul>
          <p>
            For example, if you want to limit the time, add a message content to
            the pagination, and enable fast skip in button pagination builder:
          </p>
          <pre
            class="prettyprint"
            onclick="copyText(this)"
          ><code class="language-javascript">const pagination = new ButtonPaginationBuilder(message)
  .setEmbeds(page1, page2)
  .setContent("This is made with spud.js!")
  .setTime(60000) // 60s
  .fastSkip(true)

pagination.send();</code></pre>
          <p>fastSkip is not supported in menu paginations.</p>
          <p>This is a result of the code used in the example above</p>
          <img
            src="https://media.discordapp.net/attachments/825656508464758809/1050598223418511491/brave_El7RqKqDJ8.png"
            alt="preview"
            class="preview"
          />
          <p>
            It's important to keep in mind that the examples shown in this guide
            only apply to message pagination. This method is not compatible with
            Discord interactions, such as slash commands. You must enable
            interaction in the pagination reply option in order to use it with
            Discord interactions. We'll cover how to do this in more detail
            later in the guide.<br />Now that we have completed the quick start
            guide, you can click on the link below to learn more about button
            pagination and menu pagination including builders, and more
            customizations options.
          </p>
          <button onclick="window.open('https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/ButtonPaginationBuilder/README.md')">
            button pagination
            <i class="fa-duotone fa-arrow-up-right-from-square"></i>
          </button>
          <button onclick="window.open('https://github.com/MrPotato30/spudjs-docs/blob/main/docs/packages/MenuPaginationBuilder/README.md')">
            menu pagination
            <i class="fa-duotone fa-arrow-up-right-from-square"></i>
          </button>
        </div>
        <div class="section">
          <h2>Help</h2>
          <p>
            If you're having trouble understanding something in the
            documentation, are experiencing any issues or problems, or just need
            a gentle nudge in the right direction, please don't hesitate to join
            our official <a href="/invite/">Support Server</a>. Our team and
            friendly community members are here to help and are happy to provide
            assistance, answer your questions, and offer support whenever you
            need it.
          </p>
