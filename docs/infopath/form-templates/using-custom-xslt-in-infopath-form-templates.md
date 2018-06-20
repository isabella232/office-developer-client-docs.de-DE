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
# <a name="using-custom-xslt-in-infopath-form-templates"></a><span data-ttu-id="d7fda-105">Verwenden von benutzerdefinierter XSLT in InfoPath-Formularvorlagen</span><span class="sxs-lookup"><span data-stu-id="d7fda-105">Using Custom XSLT in InfoPath Form Templates</span></span>

<span data-ttu-id="d7fda-106">Sie können die meisten Ansichtselemente erstellen, die Sie möglicherweise in Microsoft InfoPath-Formulardesigner benötigen.</span><span class="sxs-lookup"><span data-stu-id="d7fda-106">You can create most of the view elements you're likely to need in the Microsoft InfoPath form designer.</span></span> <span data-ttu-id="d7fda-107">Wenn Sie eine benutzerdefinierte Ansichtselement, die InfoPath nicht erstellt werden kann benötigen, können Sie jedoch manuell die XSL-Transformation (XSLT) ändern, die InfoPath verwendet, um die Ansicht zu generieren.</span><span class="sxs-lookup"><span data-stu-id="d7fda-107">If you need a custom view element that InfoPath can't create for you, however, you can manually modify the XSL Transformation (XSLT) that InfoPath uses to generate the view.</span></span> <span data-ttu-id="d7fda-108">Hierzu extrahieren Sie das Formular in seine Komponentendateien mithilfe von **Quelldateien exportieren** auf der Registerkarte **Veröffentlichen** , von der Microsoft Office Backstage, und klicken Sie dann bearbeiten Sie die Transformation in Ihrem bevorzugten XML-Editor wie Microsoft Visual Studio oder Editor.</span><span class="sxs-lookup"><span data-stu-id="d7fda-108">To do so, extract the form into its component files by using **Export Source Files** on the **Publish** tab of the Microsoft Office Backstage, and then edit the transform in your preferred XML editor, such as Microsoft Visual Studio or Notepad.</span></span> 
  
<span data-ttu-id="d7fda-109">Wenn Sie Änderungen an einer Ansichtstransformation außerhalb von InfoPath vornehmen und klicken Sie dann die Ansicht im Entwurfsmodus öffnen und ändern, überschreibt InfoPath die Änderungen, die Sie manuell vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="d7fda-109">If you make changes to a view transform outside of InfoPath and then open the view in design mode and make changes, InfoPath will overwrite the changes you made manually.</span></span> <span data-ttu-id="d7fda-110">Um zu verhindern, dass InfoPath und überschreiben Sie die Änderungen, die Sie vornehmen, müssen Sie diese Änderungen in Platzieren eines `<xsl:template>` Element in der Transformation und Verwendung der `xd:preserve` Modus, wie hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="d7fda-110">To keep InfoPath from overwriting the changes you make, you must place those changes in an  `<xsl:template>` element in the transform and use the  `xd:preserve` mode, as shown here:</span></span> 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

<span data-ttu-id="d7fda-111">Wenn Sie die Vorlage in die transformierte Datei einzuschließen, verwenden Sie die `<xsl:apply-templates>` Element mit demselben `xd:preserve` Modus:</span><span class="sxs-lookup"><span data-stu-id="d7fda-111">To include the template in the transformed file, use the  `<xsl:apply-templates>` element with the same  `xd:preserve` mode:</span></span> 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

<span data-ttu-id="d7fda-112">Elemente und Konstrukte in XSL-Vorlagen mit definiert die `xd:preserve` Modus wird in der InfoPath-Design-Umgebung nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d7fda-112">Elements and constructs defined within XSL templates with the  `xd:preserve` mode will not be displayed in the InfoPath design environment.</span></span> <span data-ttu-id="d7fda-113">Stattdessen wird InfoPath im benutzerdefinierten Abschnitt mit dem Steuerelement mit der Bezeichnung **Geschützter Codeabschnitt** mit einem roten Rahmen markiert.</span><span class="sxs-lookup"><span data-stu-id="d7fda-113">Instead, InfoPath will mark the custom section with a control labeled **Preserve Code Block** with a red border.</span></span> <span data-ttu-id="d7fda-114">Wenn ein Benutzer das Formular, um es auszufüllen geöffnet wird, die benutzerdefinierten XSL-Transformationen werden angewendet und die **Geschützter Codeabschnitt** -Steuerelemente werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7fda-114">When a user opens the form to fill it out, the custom XSL transforms are applied and the **Preserve Code Block** controls will not appear.</span></span> 
  

