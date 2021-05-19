---
title: SetField-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: Mit der FestlegenFeld -Aktion können Sie einem Feld einen Wert zuweisen.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432926"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="616d7-103">SetField-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="616d7-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="616d7-104">Mit der **FestlegenFeld** -Aktion können Sie einem Feld einen Wert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="616d7-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="616d7-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="616d7-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="616d7-107">Die **FestlegenFeld**-Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="616d7-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="616d7-108">Setting</span><span class="sxs-lookup"><span data-stu-id="616d7-108">Setting</span></span>

<span data-ttu-id="616d7-109">Die **FestlegenFeld**-Aktion kann mit den in der folgenden Tabelle aufgeführten Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="616d7-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="616d7-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="616d7-110">**Argument name**</span></span>|<span data-ttu-id="616d7-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="616d7-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="616d7-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="616d7-112">**Name**</span></span> <br/> |<span data-ttu-id="616d7-113">Eine Zeichenfolge, die das Feld bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="616d7-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="616d7-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="616d7-114">**Value**</span></span> <br/> |<span data-ttu-id="616d7-115">Ein Ausdruck, der den Wert angibt, der dem Feld zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="616d7-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="616d7-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="616d7-116">Remarks</span></span>

<span data-ttu-id="616d7-117">Die **SetField-Aktion** kann nicht außerhalb eines **[CreateRecord-](createrecord-data-block-access-custom-web-app.md)** oder **[EditRecord-Datenblocks](editrecord-data-block-access-custom-web-app.md)** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="616d7-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  

