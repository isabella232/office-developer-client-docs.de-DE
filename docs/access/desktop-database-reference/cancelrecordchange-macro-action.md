---
title: CancelRecordChange-Makroaktion
TOCTitle: CancelRecordChange macro action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb414837696eecc028d864c1efa9f74251f596a3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919332"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="41b7f-102">CancelRecordChange-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="41b7f-102">CancelRecordChange macro action</span></span>


<span data-ttu-id="41b7f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41b7f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41b7f-104">Mit der **CancelRecordChange** -Aktion können Sie die Änderungen an einem Datensatz in einem **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblock abbrechen, bevor für diese ein Commit erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="41b7f-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="41b7f-105">[!HINWEIS] Die **AbbrechenDatensatzänderung** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41b7f-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="41b7f-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="41b7f-106">Remarks</span></span>

<span data-ttu-id="41b7f-107">Wenn Sie die **AbbrechenDatensatzänderung** -Aktion aufrufen, wird der **DatensatzErstellen** - oder **DatensatzBearbeiten** -Datenblock sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="41b7f-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

