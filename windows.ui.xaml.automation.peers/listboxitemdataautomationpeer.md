---
-api-id: T:Windows.UI.Xaml.Automation.Peers.ListBoxItemDataAutomationPeer
-api-type: winrt class
---

<!-- Class syntax.
public class ListBoxItemDataAutomationPeer : Windows.UI.Xaml.Automation.Peers.SelectorItemAutomationPeer, Windows.UI.Xaml.Automation.Peers.IListBoxItemDataAutomationPeer, Windows.UI.Xaml.Automation.Provider.IScrollItemProvider
-->

# Windows.UI.Xaml.Automation.Peers.ListBoxItemDataAutomationPeer

## -description
Exposes [ListBox](../windows.ui.xaml.controls/listbox.md) items to Microsoft UI Automation, using a data representation of the item so that the peer supports scrolling to that item with data awareness.

## -remarks
 [ListBoxItemDataAutomationPeer](listboxitemdataautomationpeer.md) is generated from [ListBoxAutomationPeer](listboxautomationpeer.md) logic, not an associated control class.

### Default peer implementation and overrides in **ListBoxItemDataAutomationPeer**

[ListBoxItemDataAutomationPeer](listboxitemdataautomationpeer.md) has overrides of **Core** methods such that the associated [AutomationPeer](automationpeer.md) methods provide peer-specific information to a Microsoft UI Automation client.

+ [GetPattern](automationpeer_getpattern.md) reports that the peer supports [PatternInterface.ScrollItem](patterninterface.md) ([IScrollItemProvider](../windows.ui.xaml.automation.provider/iscrollitemprovider.md)). The base [SelectorItemAutomationPeer](selectoritemautomationpeer.md) supports [PatternInterface.SelectionItem](patterninterface.md) ([ISelectionItemProvider](../windows.ui.xaml.automation.provider/iselectionitemprovider.md)) and the base [ItemAutomationPeer](itemautomationpeer.md) supports [PatternInterface.VirtualizedItem](patterninterface.md) ([IVirtualizedItemProvider](../windows.ui.xaml.automation.provider/ivirtualizeditemprovider.md)).
+ [GetClassName](automationpeer_getclassname.md) returns "ListBoxItem".
+ [GetAutomationControlType](automationpeer_getautomationcontroltype.md) returns [AutomationControlType.ListItem](automationcontroltype.md).
+ Although [ItemAutomationPeer](itemautomationpeer.md) reported [IVirtualizedItemProvider](../windows.ui.xaml.automation.provider/ivirtualizeditemprovider.md) support, [ListBoxItemDataAutomationPeer](listboxitemdataautomationpeer.md) re-implements this to call [ScrollIntoView](listboxitemdataautomationpeer_scrollintoview.md).

<!--TODO investigate whether there is a default Name forwarding. There was something sticky with data bound items not being able to add Name into a tree, but maybe that is separate from the 'data' concept here-->
The peer also has other behaviors that are provided by the base [FrameworkElementAutomationPeer](frameworkelementautomationpeer.md) class. For more info, see "Base implementation in FrameworkElementAutomationPeer" section of [Custom automation peers](http://msdn.microsoft.com/library/aa8da53b-fe6e-40ac-9f0a-cb09637c87b4).

## -examples

## -see-also
[SelectorItemAutomationPeer](selectoritemautomationpeer.md), [ItemAutomationPeer](itemautomationpeer.md), [IVirtualizedItemProvider](../windows.ui.xaml.automation.provider/ivirtualizeditemprovider.md), [ISelectionItemProvider](../windows.ui.xaml.automation.provider/iselectionitemprovider.md), [IScrollItemProvider](../windows.ui.xaml.automation.provider/iscrollitemprovider.md)