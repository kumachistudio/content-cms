---
layout: default
---
# side bar
the sidebar is using position fixed. 
I personally think it would be better if we used flex box.
the side bar does not control its collapsed state. 
It recieves its collapsed state from the parent component as seen in the code below:

```javascript
/**
 * This class represents the lazy loaded LeftSidebarComponent.
 */
@Component({
  selector: 'app-sd-left-sidebar',
  templateUrl: 'left-sidebar.component.html',
  styleUrls: ['left-sidebar.component.scss']
})
export class LeftSidebarComponent {
  @Input() menuCollapsed = false;
}
```