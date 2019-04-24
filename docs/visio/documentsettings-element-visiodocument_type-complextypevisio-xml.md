---
title: DocumentSettings-Element (VisioDocument_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Enthält Elemente, die Dokumenteinstellungen angeben.
ms.openlocfilehash: e86dc5a0875006cb8bd1bbaffd36037a07fd5c0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315218"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>DocumentSettings-Element (VisioDocument_Type complexType) (' Visio XML ')

Enthält Elemente, die Dokumenteinstellungen angeben.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Das Stammelement eines Microsoft Visio-Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Eine MIME (Multipurpose Internet Mail Extensions)-codierte Microsoft Visio-Benutzeroberfläche (VSU), die benutzerdefinierte Symbolleisten darstellt.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Enthält den Namen der Microsoft Visio-Benutzeroberflächendatei (VSU), in der benutzerdefinierte Menüs und Schnellinfos für ein Dokument definiert werden.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Enthält den Namen der Microsoft Visio-Benutzeroberflächendatei (VSU), in der benutzerdefinierte Symbolleisten und Statusleisten für ein Dokument definiert werden.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Gibt an, ob das dynamische Raster Feature für ein Dokument oder Fenster aktiviert ist.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte an, bei denen der Klebstoff im Dokument aktiviert ist.  <br/> |
|[Protectbkgnd](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Gibt an, ob der Benutzer das Löschen oder Bearbeiten von Hintergrundseiten verhindert wird.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Gibt an, ob der Benutzer verhindert, dass Masters erstellt, bearbeitet oder gelöscht werden. Unabhängig von dieser Einstellung kann der Benutzer weiterhin Instanzen von Mastern erstellen.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Gibt an, ob verhindert werden soll, dass der Benutzer Shapes auswählt, deren **"LockSelect** -Element auf 1 festgelegt ist.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Gibt an, ob verhindert werden soll, dass der Benutzerformat Vorlagen erstellt oder bearbeitet.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **SnapAngle** -Elementen.  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Gibt an, ob eine bestimmte Ausrichtungs Erweiterungseinstellung für das aktive Fenster aktiviert oder deaktiviert ist.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte an, bei denen die Formen einrasten, wenn Snap im Fenster aktiv ist.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines **Stylesheet** -Elements an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|DefaultGuideStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines **Stylesheet** -Elements an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|DefaultLineStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines **Stylesheet** -Elements an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|DefaultTextStyle  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines **Stylesheet** -Elements an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ToPage  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt die ID der Seite an, die angezeigt werden soll, wenn das Dokument von Microsoft Visio geöffnet wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

