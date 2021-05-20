---
title: Verwenden von benutzerdefinierter XSLT in InfoPath-Formularvorlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Sie können die meisten Ansichtselemente erstellen, die Sie wahrscheinlich im Microsoft InfoPath-Formular-Designer benötigen. Falls Sie ein benutzerdefiniertes Ansichtselement benötigen, das nicht von InfoPath erstellt werden kann, können Sie jedoch die XSL-Transformation (XSLT) manuell ändern, mit deren Hilfe von InfoPath die Ansicht erstellt wird. Extrahieren Sie dazu das Formular in seine Komponentendateien, indem Sie Quelldateien exportieren auf der Registerkarte Veröffentlichen der Microsoft Office-Backstage verwenden, und bearbeiten Sie dann die Transformation im bevorzugten XML-Editor, z. B. Microsoft Visual Studio oder Editor.
ms.openlocfilehash: a61980191dbedeec33b06ad8173ce50126fea781
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428270"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a>Verwenden von benutzerdefinierter XSLT in InfoPath-Formularvorlagen

Sie können die meisten Ansichtselemente erstellen, die Sie wahrscheinlich im Microsoft InfoPath-Formular-Designer benötigen. Falls Sie ein benutzerdefiniertes Ansichtselement benötigen, das nicht von InfoPath erstellt werden kann, können Sie jedoch die XSL-Transformation (XSLT) manuell ändern, mit deren Hilfe von InfoPath die Ansicht erstellt wird. Extrahieren Sie dazu das Formular in seine  Komponentendateien,  indem Sie Quelldateien exportieren auf der Registerkarte Veröffentlichen der Microsoft Office-Backstage verwenden, und bearbeiten Sie dann die Transformation im bevorzugten XML-Editor, z. B. Microsoft Visual Studio oder Editor. 
  
Wenn Sie eine Ansichtstransformation außerhalb von InfoPath ändern und anschließend die Ansicht im Designmodus öffnen und Änderungen vornehmen, werden Ihre manuellen Änderungen von InfoPath überschrieben. Damit InfoPath die von Ihnen vorgenommenen Änderungen nicht überschreiben kann, müssen Sie diese Änderungen in einem Element in der Transformation platzieren und den Modus verwenden, wie  `<xsl:template>`  `xd:preserve` hier gezeigt: 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

Wenn Sie die Vorlage in die transformierte Datei einfügen möchten, verwenden Sie das  `<xsl:apply-templates>` Element im gleichen  `xd:preserve` Modus: 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

Elemente und Konstrukte, die in XSL-Vorlagen mit dem Modus definiert sind, werden in der  `xd:preserve` InfoPath-Entwurfsumgebung nicht angezeigt. Stattdessen wird der benutzerdefinierte Abschnitt von InfoPath mit dem Steuerelement **Geschützter Codeabschnitt** mit einem roten Rand markiert. Wenn ein Benutzer das Formular zum Ausfüllen öffnet, werden die benutzerdefinierten XSL-Transformationen angewendet, und die Steuerelemente **Geschützter Codeabschnitt** werden nicht angezeigt. 
  

