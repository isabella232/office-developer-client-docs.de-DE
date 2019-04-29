---
title: Zelle "LockCustProp" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: Bestimmt, ob der Benutzer im Dialogfeld Shape-Daten definieren oder im Kontextmenü für das Fenster Shape-Daten Shape-Daten auf der Benutzeroberfläche hinzufügen, löschen oder ändern darf.
ms.openlocfilehash: 001123f3bd08d35f6f8e4874e20f2ee073835494
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422523"
---
# <a name="lockcustprop-cell-protection-section"></a><span data-ttu-id="5f496-103">Zelle "LockCustProp" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="5f496-103">LockCustProp Cell (Protection Section)</span></span>

<span data-ttu-id="5f496-104">Bestimmt, ob der Benutzer im Dialogfeld **Shape-Daten definieren** oder im Kontextmenü für das Fenster **Shape-Daten** Shape-Daten auf der Benutzeroberfläche hinzufügen, löschen oder ändern darf.</span><span class="sxs-lookup"><span data-stu-id="5f496-104">Determines whether the user can add, delete, or modify shape data in the user interface (UI) by using the **Define Shape Data** dialog box or the shortcut menu for the **Shape Data** window.</span></span> 
  
|<span data-ttu-id="5f496-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5f496-105">**Value**</span></span>|<span data-ttu-id="5f496-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5f496-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5f496-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5f496-107">TRUE</span></span>  <br/> |<span data-ttu-id="5f496-108">Der Befehl **Shape-Daten definieren** im Kontextmenü des Fensters **Shape-Daten** ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5f496-108">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is disabled.</span></span>  <br/> |
|<span data-ttu-id="5f496-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5f496-109">FALSE</span></span>  <br/> |<span data-ttu-id="5f496-110">Der Befehl **Shape-Daten definieren** im Kontextmenü des Fensters **Shape-Daten** ist aktiviert (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="5f496-110">The **Define Shape Data** command on the shortcut menu in the **Shape Data** window is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5f496-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f496-111">Remarks</span></span>

<span data-ttu-id="5f496-112">Der Wert TRUE verhindert nicht, dass der Wert eines Shape-Datenelements oder der Abschnitt Shape Data im ShapeSheet-Fenster geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f496-112">A value of TRUE does not prevent a user from changing the value of a shape data item or changing the Shape Data section in the ShapeSheet window.</span></span> 
  
<span data-ttu-id="5f496-113">Wenn Sie einen Verweis auf die Zelle Zelle LockCustProp aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5f496-113">To get a reference to the LockCustProp cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f496-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5f496-114">Cell name:</span></span>  <br/> |<span data-ttu-id="5f496-115">Zelle LockCustProp</span><span class="sxs-lookup"><span data-stu-id="5f496-115">LockCustProp</span></span>  <br/> |
   
<span data-ttu-id="5f496-116">Wenn Sie einen Verweis auf die Zelle Zelle LockCustProp aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5f496-116">To get a reference to the LockCustProp cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5f496-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5f496-117">Section index:</span></span>  <br/> |<span data-ttu-id="5f496-118">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5f496-118">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5f496-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5f496-119">Row index:</span></span>  <br/> |<span data-ttu-id="5f496-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="5f496-120">**visRowLock**</span></span> <br/> |
|<span data-ttu-id="5f496-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5f496-121">Cell index:</span></span>  <br/> |<span data-ttu-id="5f496-122">**visLockCustProp**</span><span class="sxs-lookup"><span data-stu-id="5f496-122">**visLockCustProp**</span></span> <br/> |
   

