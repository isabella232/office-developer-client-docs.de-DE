---
title: Verwenden von benutzerdefinierter XSLT in InfoPath-Formularvorlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Sie können die meisten Ansichtselemente erstellen, die Sie möglicherweise in Microsoft InfoPath-Formulardesigner benötigen. Wenn Sie eine benutzerdefinierte Ansichtselement, die InfoPath nicht erstellt werden kann benötigen, können Sie jedoch manuell die XSL-Transformation (XSLT) ändern, die InfoPath verwendet, um die Ansicht zu generieren. Hierzu extrahieren Sie das Formular in seine Komponentendateien mithilfe von Quelldateien auf der Registerkarte veröffentlichen, von der Microsoft Office Backstage exportieren, und klicken Sie dann bearbeiten Sie die Transformation in Ihrem bevorzugten XML-Editor wie Microsoft Visual Studio oder Editor.
ms.openlocfilehash: 796115c99c81fc2a77812d91d317f5ce9ed54e5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790847"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a>Verwenden von benutzerdefinierter XSLT in InfoPath-Formularvorlagen

Sie können die meisten Ansichtselemente erstellen, die Sie möglicherweise in Microsoft InfoPath-Formulardesigner benötigen. Wenn Sie eine benutzerdefinierte Ansichtselement, die InfoPath nicht erstellt werden kann benötigen, können Sie jedoch manuell die XSL-Transformation (XSLT) ändern, die InfoPath verwendet, um die Ansicht zu generieren. Hierzu extrahieren Sie das Formular in seine Komponentendateien mithilfe von **Quelldateien exportieren** auf der Registerkarte **Veröffentlichen** , von der Microsoft Office Backstage, und klicken Sie dann bearbeiten Sie die Transformation in Ihrem bevorzugten XML-Editor wie Microsoft Visual Studio oder Editor. 
  
Wenn Sie Änderungen an einer Ansichtstransformation außerhalb von InfoPath vornehmen und klicken Sie dann die Ansicht im Entwurfsmodus öffnen und ändern, überschreibt InfoPath die Änderungen, die Sie manuell vorgenommen. Um zu verhindern, dass InfoPath und überschreiben Sie die Änderungen, die Sie vornehmen, müssen Sie diese Änderungen in Platzieren eines `<xsl:template>` Element in der Transformation und Verwendung der `xd:preserve` Modus, wie hier gezeigt: 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

Wenn Sie die Vorlage in die transformierte Datei einzuschließen, verwenden Sie die `<xsl:apply-templates>` Element mit demselben `xd:preserve` Modus: 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

Elemente und Konstrukte in XSL-Vorlagen mit definiert die `xd:preserve` Modus wird in der InfoPath-Design-Umgebung nicht angezeigt werden. Stattdessen wird InfoPath im benutzerdefinierten Abschnitt mit dem Steuerelement mit der Bezeichnung **Geschützter Codeabschnitt** mit einem roten Rahmen markiert. Wenn ein Benutzer das Formular, um es auszufüllen geöffnet wird, die benutzerdefinierten XSL-Transformationen werden angewendet und die **Geschützter Codeabschnitt** -Steuerelemente werden nicht angezeigt. 
  

