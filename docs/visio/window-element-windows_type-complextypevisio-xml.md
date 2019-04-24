---
title: Window-Element (Windows_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Repräsentiert ein geöffnetes Fenster in einer Instanz von Microsoft Visio. Dieses Element enthält Informationen, die erforderlich sind, um ein Benutzeroberflächenfenster im Anwendungsarbeitsbereich genau neu zu erstellen, wenn die Datei anfänglich von Visio geöffnet wird.
ms.openlocfilehash: 676818ddea7747a17b0fe296da515e80c4ffd98f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339900"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Window-Element (Windows_Type complexType) (' Visio XML ')

Repräsentiert ein geöffnetes Fenster in einer Instanz von Microsoft Visio. Dieses Element enthält Informationen, die erforderlich sind, um ein Benutzeroberflächenfenster im Anwendungsarbeitsbereich genau neu zu erstellen, wenn die Datei anfänglich von Visio geöffnet wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Windows. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Enthält die **Window** -Elemente für ein Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Gibt an, ob das dynamische Raster Feature für ein Dokument oder Fenster aktiviert ist.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte an, bei denen der Klebstoff im Dokument aktiviert ist.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Gibt an, ob Verbindungspunkte in einem Fenster angezeigt werden.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Gibt an, ob ein Raster im Zeichnungsfenster angezeigt wird.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Gibt an, ob Führungslinien im Zeichnungsfenster angezeigt werden.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Gibt an, ob Seitenumbrüche in einem Fenster angezeigt werden.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Gibt an, ob Lineale im Zeichnungsfenster angezeigt werden.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **SnapAngle** -Elementen.  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Gibt an, ob eine bestimmte Ausrichtungs Erweiterungseinstellung für das aktive Fenster aktiviert oder deaktiviert ist.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte an, bei denen die Formen einrasten, wenn Snap im Fenster aktiv ist.  <br/> |
|[Stencilgroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Gibt die Gruppe der zusammengeführten Schablonenfenster an, deren Mitglied das Fenster ist.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Enthält eine ganze Zahl, die die relative Position einer Schablone innerhalb einer Gruppe in einem Fenster angibt.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Gibt die Breite des Seitenregister Steuerelements eines Zeichnungsfensters an (als Bruchteil der Gesamtbreite des Zeichnungsfensters).  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |ID des Containers: Seite, Blatt oder Master. Nur relevant und erforderlich, **** wenn ContainerType angegeben wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ContainerType  <br/> |XSD: Token  <br/> |Optional  <br/> |MöglicherWeise handelt es sich um einen der folgenden Werte: Document, Page oder Master. Nur relevant, **** wenn WindowType als Zeichnung oder Blatt angegeben wird.  <br/> |Werte des XSD: Token-Typs.  <br/> |
|Dokument  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Dateipfad des Dokuments, das in diesem Fenster angezeigt wird.  <br/> |Werte des XSD: String-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Master  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Master-ID, wenn in diesem Fenster ein Master angezeigt wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Seite  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Seiten-ID, wenn in diesem Fenster eine Seite angezeigt wird. Relevant nur, **** wenn WindowType als Drawing angegeben wird **** und ContainerType als Page angegeben wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ParentWindow  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die ID des Fensters, in dem dieses Schablonenfenster enthalten ist. Nur relevant, **** wenn WindowType als Schablone angegeben wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ReadOnly  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Schreibgeschütztes Flag, wenn es sich bei dieser Schablone nicht um eine Dokumentschablone handelt.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|Blatt  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die ID des Blatts im Container. Nur relevant, wenn der Container als Blatt angegeben wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ViewCenterX  <br/> |XSD: Double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, die eine neue Ansicht (Fenster) beim anfänglichen öffnen annimmt.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ViewCenterY  <br/> |XSD: Double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, die eine neue Ansicht (Fenster) beim anfänglichen öffnen annimmt.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ViewScale  <br/> |XSD: Double  <br/> |Optional  <br/> |Der Standard Vergrößerungsfaktor, der verwendet wird, wenn eine neue Ansicht (Fenster) der Seite geöffnet wird. Beispiel: 1 = 100%; 1,5 = 150% usw.  <br/> |Werte des Typs XSD: Double.  <br/> |
|WindowHeight  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Höhe des Fensterrechtecks.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|WindowLeft  <br/> |XSD: kurz  <br/> |Optional  <br/> |Linke Koordinate des Fensterrechtecks.  <br/> |Werte des XSD: Short-Typs.  <br/> |
|WindowState  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Eine ganze Zahl, die Bitflags angibt.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|WindowTop  <br/> |XSD: kurz  <br/> |Optional  <br/> |Obere Koordinate des Fensterrechtecks.  <br/> |Werte des XSD: Short-Typs.  <br/> |
|WindowType  <br/> |XSD: Token  <br/> |erforderlich  <br/> |Ein Aufzählungswert, der einer der folgenden Werte sein kann: Drawing, Sheet, Stencil, or Icon.  <br/> |Werte des XSD: Token-Typs.  <br/> |
|WindowWidth  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Breite des Fensterrechtecks.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

