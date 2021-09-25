---
title: Verwenden von benutzerdefinierter XSLT in InfoPath-Formularvorlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Sie können die meisten Ansichtselemente erstellen, die Sie wahrscheinlich im Microsoft InfoPath-Formular-Designer benötigen. Falls Sie ein benutzerdefiniertes Ansichtselement benötigen, das nicht von InfoPath erstellt werden kann, können Sie jedoch die XSL-Transformation (XSLT) manuell ändern, mit deren Hilfe von InfoPath die Ansicht erstellt wird. Extrahieren Sie dazu das Formular mithilfe der Registerkarte "Quelldateien exportieren" der Microsoft Office Backstage in die Komponentendateien, und bearbeiten Sie die Transformation dann in Ihrem bevorzugten XML-Editor, z. B. Microsoft Visual Studio oder Editor.
ms.openlocfilehash: 6f25005eb69ce298f79082273eb9d21e3acf34f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621241"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a>Verwenden von benutzerdefinierter XSLT in InfoPath-Formularvorlagen

Sie können die meisten Ansichtselemente erstellen, die Sie wahrscheinlich im Microsoft InfoPath-Formular-Designer benötigen. Falls Sie ein benutzerdefiniertes Ansichtselement benötigen, das nicht von InfoPath erstellt werden kann, können Sie jedoch die XSL-Transformation (XSLT) manuell ändern, mit deren Hilfe von InfoPath die Ansicht erstellt wird. Extrahieren Sie dazu das Formular mithilfe der Registerkarte **"Quelldateien** **exportieren"** der Microsoft Office Backstage in die Komponentendateien, und bearbeiten Sie die Transformation dann in Ihrem bevorzugten XML-Editor, z. B. Microsoft Visual Studio oder Editor. 
  
Wenn Sie eine Ansichtstransformation außerhalb von InfoPath ändern und anschließend die Ansicht im Designmodus öffnen und Änderungen vornehmen, werden Ihre manuellen Änderungen von InfoPath überschrieben. Damit InfoPath die von Ihnen vorgenommenen Änderungen nicht überschreiben kann, müssen Sie diese Änderungen in einem Element in der Transformation platzieren  `<xsl:template>` und den  `xd:preserve` Modus verwenden, wie hier gezeigt: 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

Verwenden Sie das Element im gleichen Modus, um die Vorlage in die transformierte Datei `<xsl:apply-templates>` einzuschließen: `xd:preserve` 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

Elemente und Konstrukte, die in XSL-Vorlagen mit dem Modus definiert  `xd:preserve` sind, werden in der InfoPath-Entwurfsumgebung nicht angezeigt. Stattdessen wird der benutzerdefinierte Abschnitt von InfoPath mit dem Steuerelement **Geschützter Codeabschnitt** mit einem roten Rand markiert. Wenn ein Benutzer das Formular zum Ausfüllen öffnet, werden die benutzerdefinierten XSL-Transformationen angewendet, und die Steuerelemente **Geschützter Codeabschnitt** werden nicht angezeigt. 
  

