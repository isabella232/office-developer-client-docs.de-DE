---
title: Window-Element (Windows_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: Repräsentiert ein geöffnetes Fenster in einer Instanz von Microsoft Visio. Dieses Element enthält Informationen, die erforderlich sind, um ein Benutzeroberflächenfenster im Anwendungsarbeitsbereich genau neu zu erstellen, wenn die Datei erstmalig von Visio geöffnet wird.
ms.openlocfilehash: 44282149246dc4bfb93e583d8db4025d63ce542b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603200"
---
# <a name="window-element-windows_type-complextype-visio-xml"></a>Window-Element (Windows_Type complexType) (Visio XML)

Repräsentiert ein geöffnetes Fenster in einer Instanz von Microsoft Visio. Dieses Element enthält Informationen, die erforderlich sind, um ein Benutzeroberflächenfenster im Anwendungsarbeitsbereich genau neu zu erstellen, wenn die Datei erstmalig von Visio geöffnet wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |windows.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Enthält die **Window-Elemente** für ein Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Gibt an, ob das dynamische Rasterfeature für ein Dokument oder Fenster aktiviert ist.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte an, an die Shapes kleben, wenn der Kleber im Dokument aktiviert ist.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Gibt an, ob Verbindungspunkte in einem Fenster angezeigt werden.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Gibt an, ob im Zeichnungsfenster ein Raster angezeigt wird.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Gibt an, ob Führungslinien im Zeichnungsfenster angezeigt werden.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Gibt an, ob Seitenumbrüche in einem Fenster angezeigt werden.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Gibt an, ob lineal im Zeichnungsfenster angezeigt werden.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **SnapAngle-Elementen.**  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Gibt an, ob eine bestimmte Einstellung für die Snap-Erweiterung für das aktive Fenster aktiviert oder deaktiviert ist.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte an, an denen Shapes angedockt werden, wenn die Ausrichtung im Fenster aktiv ist.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Gibt die Gruppe der zusammengeführten Schablonenfenster an, deren Mitglied das Fenster ist.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Enthält eine ganze Zahl, die die relative Position einer Schablone innerhalb einer Gruppe in einem Fenster angibt.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Gibt die Breite des Seitenregisterkartensteuerelements eines Zeichnungsfensters an (als Bruchteil der Gesamtbreite des Zeichnungsfensters).  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |ID des Containers: Seite, Blatt oder Master. Nur relevant und erforderlich, wenn **ContainerType** angegeben ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ContainerType  <br/> |xsd:token  <br/> |Optional  <br/> |Kann einer der folgenden Werte sein: Dokument, Seite oder Master. Nur relevant, wenn **WindowType** als Zeichnung oder Blatt angegeben wird.  <br/> |Werte des Typs "xsd:token".  <br/> |
|Dokument  <br/> |xsd:string  <br/> |Optional  <br/> |Dateipfad des Dokuments, das in diesem Fenster angezeigt wird.  <br/> |Werte des Typs "xsd:string".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Master-ID, wenn in diesem Fenster ein Master angezeigt wird.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Seite  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Seiten-ID, wenn in diesem Fenster eine Seite angezeigt wird. Nur relevant, wenn **WindowType** als Zeichnung und **ContainerType** als Seite angegeben ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ParentWindow  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |DIE ID des Fensters, in dem dieses Schablonenfenster enthalten ist. Nur relevant, wenn **WindowType** als Schablone angegeben wird.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ReadOnly  <br/> |xsd:boolean  <br/> |Optional  <br/> |Schreibgeschütztes Kennzeichen, wenn es sich bei dieser Schablone nicht um eine Dokumentschablone handelt.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|Blatt  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |ID des Blatts im Container. Nur relevant, wenn Container als Sheet angegeben ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, von der eine neue Ansicht (fenster) beim ersten Öffnen ausgeht.  <br/> |Werte des Typs "xsd:double".  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, von der eine neue Ansicht (fenster) beim ersten Öffnen ausgeht.  <br/> |Werte des Typs "xsd:double".  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |Optional  <br/> |Der standardmäßige Vergrößerungsfaktor, der beim Öffnen einer neuen Ansicht (eines Fensters) der Seite verwendet werden soll. Beispiel: 1 = 100 %; 1,5 = 150 % usw.  <br/> |Werte des Typs "xsd:double".  <br/> |
|WindowHeight  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Höhe des Fensterrechtecks.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|WindowLeft  <br/> |xsd:short  <br/> |Optional  <br/> |Linke Koordinate des Fensterrechtecks.  <br/> |Werte des Typs "xsd:short".  <br/> |
|WindowState  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Eine ganze Zahl, die Bitkennzeichen angibt.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|WindowTop  <br/> |xsd:short  <br/> |Optional  <br/> |Obere Koordinate des Fensterrechtecks.  <br/> |Werte des Typs "xsd:short".  <br/> |
|Windowtype  <br/> |xsd:token  <br/> |Erforderlich  <br/> |Ein aufgezählter Wert, der einer der folgenden Werte sein kann: Zeichnen, Blatt, Schablone oder Symbol.  <br/> |Werte des Typs "xsd:token".  <br/> |
|WindowWidth  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Breite des Fensterrechtecks.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

