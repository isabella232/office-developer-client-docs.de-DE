---
title: CancelRecordChange-Makroaktion (benutzerdefinierte Access-Web-App)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: cbdbee8c-70d6-45df-a56b-5f7c6e5bdc6d
description: Mit der CancelRecordChange -Aktion können Sie die Änderungen an einem Datensatz in einem DatensatzErstellen - oder BearbeitenDatensatz -Datenblock abbrechen, bevor für diese ein Commit erfolgt ist.
ms.openlocfilehash: fe95718e752513c4b8b700f331fec7b78092e553
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411827"
---
# <a name="cancelrecordchange-macro-action-access-custom-web-app"></a><span data-ttu-id="00922-103">CancelRecordChange-Makroaktion (benutzerdefinierte Access-Web-App)</span><span class="sxs-lookup"><span data-stu-id="00922-103">CancelRecordChange Macro Action (Access custom web app)</span></span>

<span data-ttu-id="00922-104">Mit der **CancelRecordChange** -Aktion können Sie die Änderungen an einem Datensatz in einem **[DatensatzErstellen](createrecord-data-block-access-custom-web-app.md)** - oder **[BearbeitenDatensatz](editrecord-data-block-access-custom-web-app.md)** -Datenblock abbrechen, bevor für diese ein Commit erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="00922-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block before the changes are committed.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="00922-p101">Das Erstellen und Verwenden von Access-Web-Apps in SharePoint wird von Microsoft nicht mehr empfohlen. Alternativ sollten Sie die Verwendung von [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) für das Erstellen von Business Solutions ohne Code für das Web und für mobile Geräte in Betracht ziehen.</span><span class="sxs-lookup"><span data-stu-id="00922-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="00922-107">Die **AbbrechenDatensatzänderung**-Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="00922-107">The **CancelRecordChange** action is available only in Data Macros.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="00922-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00922-108">Remarks</span></span>

<span data-ttu-id="00922-109">Wenn Sie die **AbbrechenDatensatzänderung** -Aktion aufrufen, wird der **DatensatzErstellen** - oder **DatensatzBearbeiten** -Datenblock sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="00922-109">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span> 
  

