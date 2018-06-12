---
title: Abbrechendatensatzänderung-Makroaktion (Access benutzerdefinierte Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: cbdbee8c-70d6-45df-a56b-5f7c6e5bdc6d
description: Die Abbrechendatensatzänderung-Aktion können Sie die Änderungen zu einem Datensatz in einem DatensatzErstellen- oder BearbeitenDatensatz-Datenblock angewendet werden, bevor die Änderungen übernommen werden.
ms.openlocfilehash: 5f5d131ce8662dbd290a30ea08594cb413791d5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790210"
---
# <a name="cancelrecordchange-macro-action-access-custom-web-app"></a><span data-ttu-id="6c6c6-103">Abbrechendatensatzänderung-Makroaktion (Access benutzerdefinierte Web app)</span><span class="sxs-lookup"><span data-stu-id="6c6c6-103">CancelRecordChange Macro Action (Access custom web app)</span></span>

<span data-ttu-id="6c6c6-104">Mit der **CancelRecordChange** -Aktion können Sie die Änderungen an einem Datensatz in einem **[DatensatzErstellen](createrecord-data-block-access-custom-web-app.md)** - oder **[BearbeitenDatensatz](editrecord-data-block-access-custom-web-app.md)** -Datenblock abbrechen, bevor für diese ein Commit erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="6c6c6-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block before the changes are committed.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6c6c6-p101">[!WICHTIG] Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="6c6c6-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6c6c6-107">[!HINWEIS] Die **AbbrechenDatensatzänderung** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c6c6-107">The **CancelRecordChange** action is available only in Data Macros.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6c6c6-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6c6c6-108">Remarks</span></span>

<span data-ttu-id="6c6c6-109">Wenn Sie die **AbbrechenDatensatzänderung** -Aktion aufrufen, wird der **DatensatzErstellen** - oder **DatensatzBearbeiten** -Datenblock sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="6c6c6-109">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span> 
  

