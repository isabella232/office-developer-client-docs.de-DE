---
title: DocumentSettings-Element (VisioDocument_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Enthält Elemente, die dokumenteinstellungen angeben.
ms.openlocfilehash: e86dc5a0875006cb8bd1bbaffd36037a07fd5c0f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396470"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>DocumentSettings-Element (VisioDocument_Type ComplexType) ("Visio XML")

Enthält Elemente, die dokumenteinstellungen angeben.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Das Stammelement eines Microsoft Visio-Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Ein MIME (Multipurpose Internet Mail Extensions) codierte Microsoft Visio-Schnittstelle (VSU) Benutzerdatei, benutzerdefinierte Symbolleisten darstellt.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Enthält den Namen der Microsoft Visio Benutzer-Schnittstelle (VSU)-Datei, die benutzerdefinierte Menüs und Zugriffstasten für ein Dokument definiert.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Enthält den Namen der Microsoft Visio Benutzer-Schnittstelle (VSU)-Datei, die benutzerdefinierte Symbolleisten und Statusleisten für ein Dokument definiert.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Gibt an, ob das dynamische Gitter-Feature für ein Dokument oder Fenster aktiviert ist.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte, denen Shapes verbunden werden, wenn die Klebefunktion im Dokument aktiviert ist.  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Gibt an, ob der Benutzer löschen oder Bearbeiten von Hintergrundblätter verhindert wird.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Gibt an, ob der Benutzer verhindert wird, erstellen, bearbeiten oder Löschen von Master-Shapes. Unabhängig von dieser Einstellung kann Benutzer weiterhin Instanzen von Master-Shapes erstellen.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Gibt an, ob der Benutzer für die Auswahl von Shapes, die ihre **LockSelect** -Element, das auf 1 festgelegt haben verhindert wird.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Gibt an, ob der Benutzer erstellen oder Bearbeiten von Stilen verhindert wird.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **SnapAngle** -Elementen.  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Gibt an, ob eine Einstellung für bestimmte Snap-In-Erweiterung aktiviert oder für das aktive Fenster deaktiviert ist.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Gibt die Objekte, die Shapes einrasten, um beim Ausrichten aktiv in das Fenster ist.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines Elements **StyleSheet** .  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|DefaultGuideStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines Elements **StyleSheet** .  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|DefaultLineStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines Elements **StyleSheet** .  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|DefaultTextStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID eines Elements **StyleSheet** .  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|TopPage  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt die ID der Seite, die angezeigt werden soll, wenn das Dokument von Microsoft Visio geöffnet ist.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
   

