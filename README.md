### javascript examples

```javascript
var incidentGR = new GlideRecord('incident');
incidentGR.addQuery('active', true);
incidentGR.addQuery('category', 'hardware');
incidentGR.addQuery('caller_id.name', 'Rick Berzle');
incidentGR.query();
while (incidentGR.next()) {
    gs.info(incidentGR.getValue('number'));
}
