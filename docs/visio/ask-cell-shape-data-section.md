---
title: Zelle "Ask" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60
localization_priority: Normal
ms.assetid: b499a5eb-db8f-ebd0-d505-c9a002205e7d
description: Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Shape-Daten einzugeben.
ms.openlocfilehash: 0aa270ff918866d8f683a6408ccd71b6a22d555d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426864"
---
# <a name="ask-cell-shape-data-section"></a><span data-ttu-id="9ba09-103">Zelle "Ask" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="9ba09-103">Ask Cell (Shape Data Section)</span></span>

<span data-ttu-id="9ba09-104">Bestimmt, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren eines Shapes aufgefordert wird, Shape-Daten einzugeben.</span><span class="sxs-lookup"><span data-stu-id="9ba09-104">Determines whether a user is queried to enter shape data for a shape when an instance is created or the shape is duplicated or copied.</span></span>
  
|<span data-ttu-id="9ba09-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9ba09-105">**Value**</span></span>|<span data-ttu-id="9ba09-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ba09-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ba09-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9ba09-107">TRUE</span></span>  <br/> |<span data-ttu-id="9ba09-108">Der Benutzer wird aufgefordert, Shape-Daten in das Dialogfeld **Shape-Daten definieren** einzugeben.</span><span class="sxs-lookup"><span data-stu-id="9ba09-108">Ask user to enter shape data in the **Define Shape Data** dialog box.</span></span>  <br/> |
|<span data-ttu-id="9ba09-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9ba09-109">FALSE</span></span>  <br/> |<span data-ttu-id="9ba09-110">Benutzer nicht zur Dateneingabe auffordern.</span><span class="sxs-lookup"><span data-stu-id="9ba09-110">Do not ask user to enter data.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ba09-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ba09-111">Remarks</span></span>

<span data-ttu-id="9ba09-112">Der Wert in dieser Zelle entspricht dem Kontrollkästchen **Beim Ablegen fragen** im Dialogfeld **Shape-Daten definieren**. (Klicken Sie mit der rechten Maustaste auf das Shape, zeigen Sie auf **Daten**, und klicken Sie dann auf **Shape-Daten definieren**.)</span><span class="sxs-lookup"><span data-stu-id="9ba09-112">The value in this cell corresponds to the **Ask on drop** check box in the **Define Shape Data** dialog box (right-click the shape, point to **Data**, and then click **Define Shape Data**).</span></span>
  
<span data-ttu-id="9ba09-113">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Ask anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="9ba09-113">To get a reference to the Ask cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ba09-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9ba09-114">Cell name:</span></span>  <br/> |<span data-ttu-id="9ba09-115">Prop. *Name*  . Überprüfen Sie, wo Prop.  *name*  ist der Name der benutzerdefinierten Eigenschaftenzeile.</span><span class="sxs-lookup"><span data-stu-id="9ba09-115">Prop. *name*  .Verify            where Prop.  *name*  is the name of the custom property row.</span></span>  <br/> |
   
<span data-ttu-id="9ba09-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Ask nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="9ba09-116">To get a reference to the Ask cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ba09-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9ba09-117">Section index:</span></span>  <br/> |<span data-ttu-id="9ba09-118">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="9ba09-118">**visSectionProp**</span></span> <br/> |
|<span data-ttu-id="9ba09-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9ba09-119">Row index:</span></span>  <br/> |<span data-ttu-id="9ba09-120">**visRowProp**  +   *i,* *wobei i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="9ba09-120">**visRowProp** +  *i*            where  *i*  = 0, 1, 2,...</span></span>  <br/> |
|<span data-ttu-id="9ba09-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9ba09-121">Cell index:</span></span>  <br/> |<span data-ttu-id="9ba09-122">**visCustPropsAsk**</span><span class="sxs-lookup"><span data-stu-id="9ba09-122">**visCustPropsAsk**</span></span> <br/> |
   

