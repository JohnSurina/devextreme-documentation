---
id: dxScheduler.Options.onAppointmentTooltipShowing
type: function(e)
default: null
---
---
##### shortDescription
Occurs before showing an appointment's tooltip.

##### param(e): ui/scheduler:AppointmentTooltipShowingEvent
Information about the event.

##### field(e.appointments): Array<Object>
An array of appointments.

##### field(e.cancel): Boolean
Allows you to prevent a tooltip from showing.

##### field(e.component): {WidgetName}
The UI component's instance.

##### field(e.element): DxElement
#include common-ref-elementparam with { element: "UI component" }

##### field(e.model): any
The model data. Available only if you use Knockout.

##### field(e.targetElement): DxElement
The target element of the tooltip.

---
