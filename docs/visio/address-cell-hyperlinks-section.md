---
title: Zelle "Address" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251387
localization_priority: Normal
ms.assetid: 3864aadd-3f86-c20e-1a74-b0aaff5106f7
description: Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.
ms.openlocfilehash: 0fbb89e18a2d7a849e2369c0d41aac4a647f067b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438036"
---
# <a name="address-cell-hyperlinks-section"></a><span data-ttu-id="375c7-103">Zelle "Address" (Abschnitt "Hyperlinks")</span><span class="sxs-lookup"><span data-stu-id="375c7-103">Address Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="375c7-104">Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.</span><span class="sxs-lookup"><span data-stu-id="375c7-104">Specifies a URL address, file name, or UNC path to which to jump.</span></span>
  
<span data-ttu-id="375c7-105">Sie können Address als relativen Pfad basierend auf dem Basispfad angeben,  der für  das Dokument im  **Feld Hyperlinkbasis** auf der Registerkarte Zusammenfassung des Dialogfelds Eigenschaften definiert ist (klicken Sie auf die Registerkarte Datei, klicken Sie auf **Info,** klicken Sie auf \*\* Eigenschaften \*\*, und klicken Sie dann auf **Erweiterte Eigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="375c7-105">You can specify Address as a relative path based on the base path defined for the document in the **Hyperlink base** box on the **Summary** tab of the **Properties** dialog box (click the **File** tab, click **Info**, click \*\* Properties \*\*, and then click **Advanced Properties**).</span></span> <span data-ttu-id="375c7-106">Wenn das Dokument keinen Basispfad hat, navigiert die Anwendung basierend auf dem Dokumentpfad.</span><span class="sxs-lookup"><span data-stu-id="375c7-106">If the document has no base path, the application navigates based on the document path.</span></span> <span data-ttu-id="375c7-107">Wenn das Dokument noch nicht gespeichert wurde, bleibt der Hyperlink undefiniert.</span><span class="sxs-lookup"><span data-stu-id="375c7-107">If the document has not been saved, the hyperlink is undefined.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="375c7-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="375c7-108">Remarks</span></span>

<span data-ttu-id="375c7-109">Sie können auch den Wert der Zelle Address im Dialogfeld  **Hyperlinks** festlegen (klicken Sie auf der Registerkarte Einfügen auf **Hyperlink).**</span><span class="sxs-lookup"><span data-stu-id="375c7-109">You can also set the value of the Address cell in the **Hyperlinks** dialog box (click **Hyperlink** on the **Insert** tab).</span></span> 
  
<span data-ttu-id="375c7-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Address nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="375c7-110">To get a reference to the Address cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="375c7-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="375c7-111">Cell name:</span></span>  <br/> |<span data-ttu-id="375c7-112">Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="375c7-112">Hyperlink.</span></span> <span data-ttu-id="375c7-113">*Name*  . Adresse, an der Hyperlink angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="375c7-113">*name*  .Address           where Hyperlink.</span></span> <span data-ttu-id="375c7-114">*Name*  ist der Name der Hyperlinkzeile</span><span class="sxs-lookup"><span data-stu-id="375c7-114">*name*  is the name of the hyperlink row</span></span>  <br/> |
   
<span data-ttu-id="375c7-115">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Address anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="375c7-115">To get a reference to the Address cell by name from another formula, or from a program, by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="375c7-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="375c7-116">Section index:</span></span>  <br/> |<span data-ttu-id="375c7-117">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="375c7-117">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="375c7-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="375c7-118">Row index:</span></span>  <br/> |<span data-ttu-id="375c7-119">**visRow1stHyperlink**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="375c7-119">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="375c7-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="375c7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="375c7-121">**visHLinkAddress**</span><span class="sxs-lookup"><span data-stu-id="375c7-121">**visHLinkAddress**</span></span> <br/> |
   

