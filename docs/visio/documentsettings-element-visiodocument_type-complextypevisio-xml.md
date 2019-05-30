---
title: DocumentSettings-Element (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Enthält Elemente, die Dokumenteinstellungen angeben.
ms.openlocfilehash: 0d8e0809afae7b3de059166343577bb58f0eb01b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540070"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>DocumentSettings-Element (VisioDocument_Type complexType) (Visio XML)

Enthält Elemente, die Dokumenteinstellungen angeben.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Das Stammelement eines Microsoft Visio Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Eine MIME-Datei (Multipurpose Internet Mail Extensions), die Microsoft Visio Benutzeroberfläche (VSU) kodiert, die benutzerdefinierte Symbolleisten darstellt.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Enthält den Namen der Microsoft Visio-Benutzeroberflächendatei (VSU), die benutzerdefinierte Menüs und Zugriffstasten für ein Dokument definiert.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Enthält den Namen der Microsoft Visio-Benutzeroberflächendatei (VSU), die benutzerdefinierte Symbolleisten und Statusleisten für ein Dokument definiert.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Gibt an, ob das dynamische Raster Feature für ein Dokument oder Fenster aktiviert ist.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte an, an die die Shapes kleben, wenn der Klebstoff im Dokument aktiviert ist.  <br/> |
|[Protectbkgnd](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Gibt an, ob verhindert werden soll, dass der Benutzer Hintergrundseiten löscht oder bearbeitet.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Gibt an, ob der Benutzer das Erstellen, bearbeiten oder Löschen von Mastervorlagen verhindert. Unabhängig von dieser Einstellung kann der Benutzer weiterhin Instanzen von Masters erstellen.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Gibt an, ob verhindert werden soll, dass der Benutzer Shapes auswählt, deren **"LockSelect** -Element auf 1 festgelegt ist.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Gibt an, ob der Benutzer das Erstellen oder Bearbeiten von Formatvorlagen verhindert.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **SnapAngle** -Elementen.  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Gibt an, ob eine bestimmte Einstellung für die Ausrichtungs Erweiterung für das aktive Fenster aktiviert oder deaktiviert ist.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte an, an denen Shapes ausgerichtet werden, wenn Snap im Fenster aktiv ist.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines **Stylesheet** -Elements an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|DefaultGuideStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines **Stylesheet** -Elements an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|DefaultLineStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines **Stylesheet** -Elements an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|DefaultTextStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines **Stylesheet** -Elements an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Startpage  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID der Seite an, die angezeigt werden soll, wenn das Dokument von Microsoft Visio geöffnet wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

