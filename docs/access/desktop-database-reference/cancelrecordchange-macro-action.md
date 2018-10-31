---
title: AbbrechenDatensatzänderung-Makroaktion
TOCTitle: CancelRecordChange Macro Action
ms:assetid: 73031240-1ff6-660b-b25f-11a880df6031
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195846(v=office.15)
ms:contentKeyID: 48545626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddf6a6eb71d60fb98d92a9ce18bfd871f298f702
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864207"
---
# <a name="cancelrecordchange-macro-action"></a><span data-ttu-id="cb690-102">AbbrechenDatensatzänderung-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="cb690-102">CancelRecordChange Macro Action</span></span>


<span data-ttu-id="cb690-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb690-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cb690-104">Mit der **CancelRecordChange** -Aktion können Sie die Änderungen an einem Datensatz in einem **[DatensatzErstellen](createrecord-data-block.md)** - oder **[BearbeitenDatensatz](editrecord-data-block.md)** -Datenblock abbrechen, bevor für diese ein Commit erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="cb690-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block.md)** or **[EditRecord](editrecord-data-block.md)** data block before the changes are committed.</span></span>


> [!NOTE]
> <span data-ttu-id="cb690-105">[!HINWEIS] Die **AbbrechenDatensatzänderung** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb690-105">The **CancelRecordChange** action is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="cb690-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cb690-106">Remarks</span></span>

<span data-ttu-id="cb690-107">Wenn Sie die **AbbrechenDatensatzänderung** -Aktion aufrufen, wird der **DatensatzErstellen** - oder **DatensatzBearbeiten** -Datenblock sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="cb690-107">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span>

