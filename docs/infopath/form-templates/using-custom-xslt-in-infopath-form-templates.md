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
# <a name="using-custom-xslt-in-infopath-form-templates"></a><span data-ttu-id="95e36-105">Verwenden von benutzerdefinierter XSLT in InfoPath-Formularvorlagen</span><span class="sxs-lookup"><span data-stu-id="95e36-105">Using Custom XSLT in InfoPath Form Templates</span></span>

<span data-ttu-id="95e36-106">Sie können die meisten Ansichtselemente erstellen, die Sie wahrscheinlich im Microsoft InfoPath-Formular-Designer benötigen.</span><span class="sxs-lookup"><span data-stu-id="95e36-106">You can create most of the view elements you're likely to need in the Microsoft InfoPath form designer.</span></span> <span data-ttu-id="95e36-107">Falls Sie ein benutzerdefiniertes Ansichtselement benötigen, das nicht von InfoPath erstellt werden kann, können Sie jedoch die XSL-Transformation (XSLT) manuell ändern, mit deren Hilfe von InfoPath die Ansicht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="95e36-107">If you need a custom view element that InfoPath can't create for you, however, you can manually modify the XSL Transformation (XSLT) that InfoPath uses to generate the view.</span></span> <span data-ttu-id="95e36-108">Extrahieren Sie dazu das Formular in seine  Komponentendateien,  indem Sie Quelldateien exportieren auf der Registerkarte Veröffentlichen der Microsoft Office-Backstage verwenden, und bearbeiten Sie dann die Transformation im bevorzugten XML-Editor, z. B. Microsoft Visual Studio oder Editor.</span><span class="sxs-lookup"><span data-stu-id="95e36-108">To do so, extract the form into its component files by using **Export Source Files** on the **Publish** tab of the Microsoft Office Backstage, and then edit the transform in your preferred XML editor, such as Microsoft Visual Studio or Notepad.</span></span> 
  
<span data-ttu-id="95e36-109">Wenn Sie eine Ansichtstransformation außerhalb von InfoPath ändern und anschließend die Ansicht im Designmodus öffnen und Änderungen vornehmen, werden Ihre manuellen Änderungen von InfoPath überschrieben.</span><span class="sxs-lookup"><span data-stu-id="95e36-109">If you make changes to a view transform outside of InfoPath and then open the view in design mode and make changes, InfoPath will overwrite the changes you made manually.</span></span> <span data-ttu-id="95e36-110">Damit InfoPath die von Ihnen vorgenommenen Änderungen nicht überschreiben kann, müssen Sie diese Änderungen in einem Element in der Transformation platzieren und den Modus verwenden, wie  `<xsl:template>`  `xd:preserve` hier gezeigt:</span><span class="sxs-lookup"><span data-stu-id="95e36-110">To keep InfoPath from overwriting the changes you make, you must place those changes in an  `<xsl:template>` element in the transform and use the  `xd:preserve` mode, as shown here:</span></span> 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

<span data-ttu-id="95e36-111">Wenn Sie die Vorlage in die transformierte Datei einfügen möchten, verwenden Sie das  `<xsl:apply-templates>` Element im gleichen  `xd:preserve` Modus:</span><span class="sxs-lookup"><span data-stu-id="95e36-111">To include the template in the transformed file, use the  `<xsl:apply-templates>` element with the same  `xd:preserve` mode:</span></span> 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

<span data-ttu-id="95e36-112">Elemente und Konstrukte, die in XSL-Vorlagen mit dem Modus definiert sind, werden in der  `xd:preserve` InfoPath-Entwurfsumgebung nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95e36-112">Elements and constructs defined within XSL templates with the  `xd:preserve` mode will not be displayed in the InfoPath design environment.</span></span> <span data-ttu-id="95e36-113">Stattdessen wird der benutzerdefinierte Abschnitt von InfoPath mit dem Steuerelement **Geschützter Codeabschnitt** mit einem roten Rand markiert.</span><span class="sxs-lookup"><span data-stu-id="95e36-113">Instead, InfoPath will mark the custom section with a control labeled **Preserve Code Block** with a red border.</span></span> <span data-ttu-id="95e36-114">Wenn ein Benutzer das Formular zum Ausfüllen öffnet, werden die benutzerdefinierten XSL-Transformationen angewendet, und die Steuerelemente **Geschützter Codeabschnitt** werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95e36-114">When a user opens the form to fill it out, the custom XSL transforms are applied and the **Preserve Code Block** controls will not appear.</span></span> 
  

