---
title: SetField-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: Die FestlegenFeld-Aktion kann verwendet werden, ein Feld einen Wert zuweisen.
ms.openlocfilehash: 1221ea408540a960b948d2d3ece272fd71cb3daf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790361"
---
# <a name="setfield-macro-action-access-custom-web-app"></a><span data-ttu-id="3fddc-103">SetField-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="3fddc-103">SetField Macro Action (Access custom web app)</span></span>

<span data-ttu-id="3fddc-104">Mit der **FestlegenFeld** -Aktion können Sie einem Feld einen Wert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="3fddc-104">The **SetField** action can be used to assign a value to a field.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="3fddc-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="3fddc-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3fddc-107">[!HINWEIS] Die **FestlegenFeld** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3fddc-107">The **SetField** action is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="3fddc-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="3fddc-108">Setting</span></span>

<span data-ttu-id="3fddc-109">Die **FestlegenFeld** -Aktion kann mit den in der folgenden Tabelle aufgeführten Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fddc-109">The **SetField** action has the arguments listed in the following table.</span></span> 
  
|<span data-ttu-id="3fddc-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="3fddc-110">**Argument name**</span></span>|<span data-ttu-id="3fddc-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3fddc-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3fddc-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="3fddc-112">**Name**</span></span> <br/> |<span data-ttu-id="3fddc-113">Eine Zeichenfolge, die das Feld bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3fddc-113">A string that identifies the field.</span></span>  <br/> |
|<span data-ttu-id="3fddc-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3fddc-114">**Value**</span></span> <br/> |<span data-ttu-id="3fddc-115">Ein Ausdruck, der angibt, den Wert in das Feld zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3fddc-115">An expression that specifies the value to assign to the field.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fddc-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3fddc-116">Remarks</span></span>

<span data-ttu-id="3fddc-117">Die **FestlegenFeld** -Aktion kann nicht außerhalb von einem **[DatensatzErstellen-](createrecord-data-block-access-custom-web-app.md)** oder **[BearbeitenDatensatz](editrecord-data-block-access-custom-web-app.md)** -Datenblock verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fddc-117">The **SetField** action cannot be used outside of a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block.</span></span> 
  

