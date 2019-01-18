---
title: CancelRecordChange-Makroaktion
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d19e7adcdd3bb60f24d90e75942fcc0b4e16e2e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718543"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="595e0-102">CancelRecordChange-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="595e0-102">CancelRecordChange macro action</span></span>


<span data-ttu-id="595e0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="595e0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="595e0-104">Mit der **CancelRecordChange** -Aktion können Sie die Änderungen an einem Datensatz in einem **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblock abbrechen, bevor für diese ein Commit erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="595e0-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="595e0-105">[!HINWEIS] Die **AbbrechenDatensatzänderung** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="595e0-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="595e0-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="595e0-106">Remarks</span></span>

<span data-ttu-id="595e0-107">Wenn Sie die **AbbrechenDatensatzänderung** -Aktion aufrufen, wird der **DatensatzErstellen** - oder **DatensatzBearbeiten** -Datenblock sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="595e0-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

