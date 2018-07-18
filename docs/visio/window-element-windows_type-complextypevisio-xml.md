---
title: Window-Element (Windows_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: da776276-e8c2-085b-9b23-e5b1f5ba64cd
description: >-
  Repräsentiert ein geöffnetes Fenster in einer Instanz von Microsoft Visio.
   Dieses Element enthält die erforderlichen Informationen, um ein Fenster auf der Benutzeroberfläche im Anwendungsarbeitsbereich genau neu erstellen, wenn die Datei Anfangs von Visio geöffnet wird.
ms.openlocfilehash: 762b689d625c7865696a0bf8bb8c4acc25e3d8eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798418"
---
# <a name="window-element-windowstype-complextype-visio-xml"></a>Window-Element (Windows_Type ComplexType) ("Visio XML")

Repräsentiert ein geöffnetes Fenster in einer Instanz von Microsoft Visio.
 Dieses Element enthält die erforderlichen Informationen, um ein Fenster auf der Benutzeroberfläche im Anwendungsarbeitsbereich genau neu erstellen, wenn die Datei Anfangs von Visio geöffnet wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Windows.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Window" type="Window_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Windows](windows-elementvisio-xml.md) <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |Enthält die Elemente des **Fensters** für ein Dokument an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DynamicGridEnabled](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Gibt an, ob das dynamische Gitter-Feature für ein Dokument oder Fenster aktiviert ist.  <br/> |
|[GlueSettings](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte, denen Shapes verbunden werden, wenn die Klebefunktion im Dokument aktiviert ist.  <br/> |
|[ShowConnectionPoints](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[ShowConnectionPoints_Type](showconnectionpoints_type-complextypevisio-xml.md) <br/> |Gibt an, ob Verbindungspunkte in einem Fenster angezeigt werden.  <br/> |
|[ShowGrid](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[ShowGrid_Type](showgrid_type-complextypevisio-xml.md) <br/> |Gibt an, ob ein Raster im Zeichnungsfenster angezeigt wird.  <br/> |
|[ShowGuides](showguides-element-window_type-complextypevisio-xml.md) <br/> |[ShowGuides_Type](showguides_type-complextypevisio-xml.md) <br/> |Gibt an, ob Führungslinien im Zeichnungsfenster angezeigt werden.  <br/> |
|[ShowPageBreaks](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[ShowPageBreaks_Type](showpagebreaks_type-complextypevisio-xml.md) <br/> |Gibt an, ob Seitenumbrüche in einem Fenster angezeigt werden.  <br/> |
|[ShowRulers](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[ShowRulers_Type](showrulers_type-complextypevisio-xml.md) <br/> |Gibt an, ob Lineale im Zeichnungsfenster angezeigt werden.  <br/> |
|[SnapAngles](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **SnapAngle** -Elementen.  <br/> |
|[SnapExtensions](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Gibt an, ob eine Einstellung für bestimmte Snap-In-Erweiterung aktiviert oder für das aktive Fenster deaktiviert ist.  <br/> |
|[SnapSettings](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte, die Shapes einrasten, um beim Ausrichten aktiv in das Fenster ist.  <br/> |
|[StencilGroup](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroup_Type](stencilgroup_type-complextypevisio-xml.md) <br/> |Gibt die Gruppe der zusammengeführten Schablonenfenster, das Fenster Mitglied ist.  <br/> |
|[StencilGroupPos](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[StencilGroupPos_Type](stencilgrouppos_type-complextypevisio-xml.md) <br/> |Enthält eine ganze Zahl, die die relative Position einer Schablone innerhalb einer Gruppe in einem Fenster angibt.  <br/> |
|[TabSplitterPos](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[TabSplitterPos_Type](tabsplitterpos_type-complextypevisio-xml.md) <br/> |Gibt die Breite des Registersteuerelements Seite eines Zeichnungsfenster (als Prozentsatz der Breite des Zeichnungsfensters) an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Container  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |ID des Containers: Seite, Blatt oder Master-Shape. Nur relevant und erforderlich, wenn **ContainerType** angegeben wird.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ContainerType  <br/> |XSD:Token  <br/> |Optional  <br/> |Kann eine der folgenden Werte sein: Dokument, Page- oder Master. Nur relevant, wenn **Fenstertyp** als Zeichnung oder Blatt angegeben ist.  <br/> |Werte des Typs Xsd:token.  <br/> |
|Document  <br/> |XSD: String  <br/> |Optional  <br/> |Dateipfad der in diesem Fenster angezeigte Dokument.  <br/> |Werte des Typs xsd: String.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements in seinem übergeordneten Element.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Master  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Master-Shape-ID, wenn in diesem Fenster ein Master-Shape angezeigt wird.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Page  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Seiten-ID, wenn dieses Fenster auf eine Seite angezeigt werden. Relevante, nur wenn **Fenstertyp** als Zeichen- und **ContainerType** angegeben wird als Seite angegeben wird.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ParentWindow  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |ID des Fensters, in dem diese Schablonenfenster enthalten ist. Nur relevant, wenn **Fenstertyp** als Schablone angegeben ist.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ReadOnly  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Schreibschutzflag Wenn die Schablone keiner Dokumentschablone ist.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|Blatt  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |ID des Blatts im Container. Nur relevant, wenn Container als Blatt angegeben ist.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |XSD: Double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite, die eine neue Ansicht (Fenster) geht davon aus, wenn es zunächst geöffnet wird.  <br/> |Werte des Typs xsd: Double.  <br/> |
|ViewCenterY  <br/> |XSD: Double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite, die eine neue Ansicht (Fenster) geht davon aus, wenn es zunächst geöffnet wird.  <br/> |Werte des Typs xsd: Double.  <br/> |
|ViewScale  <br/> |XSD: Double  <br/> |Optional  <br/> |Der Standardwert Vergrößerungsfaktor verwendet, wenn eine neue Ansicht (Fenster) auf der Seite geöffnet wird. Beispiel: 1 = 100 %; 1,5 = 150 % und So weiter.  <br/> |Werte des Typs xsd: Double.  <br/> |
|WindowHeight  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die Höhe des Rechtecks Fenster.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|WindowLeft  <br/> |XSD:Short  <br/> |Optional  <br/> |Linke Koordinate des Rechtecks Fenster.  <br/> |Werte des Typs Xsd:short.  <br/> |
|WindowState  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Eine ganze Zahl angeben bit Kennzeichen.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|WindowTop  <br/> |XSD:Short  <br/> |Optional  <br/> |Oberste Koordinate des Rechtecks Fenster.  <br/> |Werte des Typs Xsd:short.  <br/> |
|Fenstertyp  <br/> |XSD:Token  <br/> |erforderlich  <br/> |Ein Aufzählungswert, der eine der folgenden möglicherweise: Zeichnung, Blatt, Schablone oder Symbol.  <br/> |Werte des Typs Xsd:token.  <br/> |
|WindowWidth  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die Breite des Rechtecks Fenster.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
   

