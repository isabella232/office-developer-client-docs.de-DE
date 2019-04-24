---
title: Update-Funktion (Access Custom Web App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Gibt zurück, ob ein Einfüge-oder Aktualisierungsvorgang für das angegebene Feld versucht wurde.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307826"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="2a0d5-103">Update-Funktion (Access Custom Web App)</span><span class="sxs-lookup"><span data-stu-id="2a0d5-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="2a0d5-104">Gibt zurück, ob ein Einfüge-oder Aktualisierungsvorgang für das angegebene Feld versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="2a0d5-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2a0d5-p101">Die in diesem Artikel beschriebene Cloudspeicherfunktion wird in Office 2013 und Office 2016 nicht mehr unterstützt und kann dazu führen, dass die folgende Fehlermeldung angezeigt wird: >  *Leider bestehen Serverprobleme, sodass wir \<Dienst\> zurzeit nicht hinzufügen können. Bitte versuchen Sie es später erneut.* > Informationen zum Cloudspeicher für Office Online, Office für iOS und Office für Android finden Sie in unserem [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="2a0d5-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2a0d5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a0d5-107">Syntax</span></span>

 <span data-ttu-id="2a0d5-108">**Update** (*Spalte*)</span><span class="sxs-lookup"><span data-stu-id="2a0d5-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="2a0d5-109">Die **Update** -Funktion enthält die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="2a0d5-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="2a0d5-110">**Argumentname**</span><span class="sxs-lookup"><span data-stu-id="2a0d5-110">**Argument name**</span></span>|<span data-ttu-id="2a0d5-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2a0d5-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2a0d5-112">*Column*</span><span class="sxs-lookup"><span data-stu-id="2a0d5-112">*Column*</span></span>  <br/> |<span data-ttu-id="2a0d5-113">Der Name des Felds, das auf einen Einfüge-oder Aktualisierungsvorgang überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a0d5-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a0d5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a0d5-114">Remarks</span></span>

<span data-ttu-id="2a0d5-115">Die **Update** -Funktion gibt true zurück, unabhängig davon, ob ein INSERT-oder Update-Versuch erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2a0d5-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

