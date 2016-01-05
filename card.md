# Markup: **card**
- diseño HTML de una tarjeta.

## Parámetros
##### id
- identificador de la tarjeta

##### type
- `image`
- `quote`
- `event`
- `news`
- `news-more`
- `iconic`
- `user`
- `dashboard-info`
- `meal`

## Sub markup's:
##### back
- define el diseño de la parte de atrás de la tarjeta

##### heading
- define el diseño del encabezado de la tarjeta

##### body
- define el diseño del cuerpo de la tarjeta

##### footer
- define el diseño del pie de la tajeta

## Ejemplos:
````
{{#card id="card-image" type="image" medium="33%" small="50%"}}
    {{#with movimiento}}
        {{body color="{{value color}}" img="picjumbo/4.jpg" opaque="80%" icon="gear-b" name="Titulo" subName="Sub Titulo"}}
    {{/with}}
{{/card}}
````

````
{{#card id="card-quote" type="quote" medium="33%" small="50%"}}
    {{#with movimiento}}
        {{#body color="black" textColor="white" icon="" img="picjumbo/9.jpg" opaque="50%" author="Ben Garratt"}}
            {{#p}}{{value nombre}}. Try to make all your work look like something Apple would do.{{/p}}
        {{/body}}
    {{/with}}
{{/card}}
````
````
{{#card id="card-event" type="event" medium="50%" small="50%"}}
    {{#with movimiento}}
        {{#body month="November" day="13" img="picjumbo/12.jpg"}}
            {{#h4}}Young Professionals London{{/h4}}
            {{#p}}A Social Networking group with an International mix of Young Professionals interested in meeting other like minded people for friendship / networking / partying at exclusive Members Clubs, Lounges & Bars. Recommended age range is 21+.{{/p}}
        {{/body}}
        {{#footer}}
            {{#div class="btn-group btn-merged btn-group-sm pull-right"}}
              {{#button type="button" class="btn btn-green btn-flat"}}Attend{{/button}}
              {{#button type="button" class="btn btn-orange btn-flat"}}Maybe{{/button}}
              {{#button type="button" class="btn btn-red btn-flat"}}Decline{{/button}}
            {{/div}}
        {{/footer}}
    {{/with}}
{{/card}}
````
````
{{#card id="card-news" type="news" medium="33%" small="50%"}}
    {{#with movimiento}}
        {{#heading color="amber" img="picjumbo/5.jpg" opaque="50%"}}
            {{#h3 class="card-title"}}{{value nombre}}{{/h3}}
        {{/heading}}
        {{#body}}
            {{#p}}Collaboratively administrate empowered markets via plug-and-play networks. Dynamically procrastinate B2C users after installed base benefits. Dramatically visualize...{{/p}}
        {{/body}}
    {{/with}}
{{/card}}
````
````
{{#card id="card-news-more" type="news-more" clickable="true" medium="33%" small="50%"}}
    {{#with movimiento}}
        {{#heading img="picjumbo/29.jpg" opaque="50%" badge="NEWS" icon="create" buttonColor="pink"}}
            Quickly maximize timely deliverables
        {{/heading}}
        {{#body}}
            {{#p}}Collaboratively administrate empowered markets via plug-and-play networks. Dynamically procrastinate B2C users after installed base benefits. Dramatically visualize customer directed convergence without revolutionary ROI.{{/p}}
            {{#p}}Efficiently unleash cross-media information without cross-media value. Quickly maximize timely deliverables for real-time schemas. Dramatically maintain clicks-and-mortar solutions without functional solutions.{{/p}}
            {{#p}}Completely synergize resource sucking relationships via premier niche markets. Professionally cultivate one-to-one customer service with robust ideas. Dynamically innovate resource-leveling customer service for state of the art customer service.{{/p}}
        {{/body}}
    {{/with}}
{{/card}}
{{#card id="card-iconic" type="iconic" medium="25%" small="50%"}}
    {{#with movimiento}}
        {{#body color="{{value color}}" icon="{{value icono}}" align="center"}}
            {{#h4}}{{value nombre}}{{/h4}}
            {{#p}}A speedometer or a speed meter is a gauge.{{/p}}
        {{/body}}
    {{/with}}
{{/card}}
````
````
{{#card id="card-user" type="user" clickable="true" medium="33%" small="50%"}}
    {{#with movimiento}}
        {{#back color="blue-grey" icon="social-buffer" iconHeight="196px"}}
            {{#h4}}{{value nombre}}{{/h4}}
            {{#p}}Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.{{/p}}
        {{/back}}
        {{#body color="{{value color}}" icon="{{value icono}}" img="{{image imagen}}"}}
            {{#h3 class="card-title"}}{{value nombre}}{{/h3}}
            {{#div class="subhead"}}Gerente de Ventas{{/div}}
            {{#p}}Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.{{/p}}
            {{#ul class="social-links"}}
                {{#li}}{{#a href="#"}}{{#i class="fa fa-github"}}{{/i}}{{/a}}{{/li}}
                {{#li}}{{#a href="#"}}{{#i class="fa fa-twitter"}}{{/i}}{{/a}}{{/li}}
                {{#li}}{{#a href="#"}}{{#i class="fa fa-facebook"}}{{/i}}{{/a}}{{/li}}
            {{/ul}}
        {{/body}}
        {{#footer}}
            {{#a class="pull-left" href="#"}}{{#small}} 8 amigos comumes{{/small}}{{/a}}                 
            {{#button class=" btn btn-xs btn-flat pull-right"}}Agregar amigo{{/button}}
        {{/footer}}
    {{/with}}
{{/card}}
{{#card id="card-dashboard-info" type="dashboard-info" medium="25%" small="50%"}}
    {{#with movimiento}}
        {{#body color="{{value color}}" icon="{{value icono}}" footerIcon="caret-up" footer="Total balance is $23,591"}}
            {{#h4}}Revenue{{/h4}}
            {{#p class="result"}}$10,786{{/p}}
        {{/body}}
    {{/with}}
{{/card}}
````
````
{{#card id="card-meal" type="meal" medium="33%" small="50%" color="{{movimiento.color}}"}}
    {{#with movimiento}}
        {{#heading}}
            {{#h3 class="card-title"}}{{value nombre}}{{/h3}}
            {{#div class="card-subhead"}}
                By {{#a href="#"}}Richard Sanders{{/a}}
            {{/div}}
        {{/heading}}
        {{#body img="picjumbo/21.jpg"}}
            {{#ul class="users"}}
                <li><a href="#" data-toggle="tooltip" data-placement="top" data-original-title="Emanuele Costa"><img src="/assets/globals/img/faces/1.jpg" alt=""></a></li>
                <li><a href="#" data-toggle="tooltip" data-placement="top" data-original-title="Sjors Huisman"><img src="/assets/globals/img/faces/2.jpg" alt=""></a></li>
                <li><a href="#" data-toggle="tooltip" data-placement="top" data-original-title="Isla Olsen"><img src="/assets/globals/img/faces/3.jpg" alt=""></a></li>
            {{/ul}}
        {{/body}}
        {{#footer}}
            {{#ul}}
                {{#li}}1,378 Students{{/li}}
                {{#li}}{{#a href="#"}}Join Them{{/a}}{{/li}}
            {{/ul}}
        {{/footer}}
    {{/with}}
{{/card}}
````