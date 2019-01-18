---
title: Flush-Methode - ActiveX Data Objects (ADO)
TOCTitle: Flush method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a55eb66c454d510d53083c495326548eda08af
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708032"
---
# <a name="flush-method-ado"></a><span data-ttu-id="1b41f-102">Flush-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="1b41f-102">Flush method (ADO)</span></span>


<span data-ttu-id="1b41f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b41f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b41f-104">Erzwingt, dass der Inhalt des im ADO-Puffer verbleibenden [Stream](stream-object-ado.md)-Objekts an das zugrundeliegende Objekt, dem das **Stream** -Objekt zugeordnet ist, übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="1b41f-104">Forces the contents of the [Stream](stream-object-ado.md) remaining in the ADO buffer to the underlying object with which the **Stream** is associated.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b41f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b41f-105">Syntax</span></span>

<span data-ttu-id="1b41f-106">*Stream-Objekt*. Leeren</span><span class="sxs-lookup"><span data-stu-id="1b41f-106">*Stream*.Flush</span></span>

## <a name="remarks"></a><span data-ttu-id="1b41f-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1b41f-107">Remarks</span></span>

<span data-ttu-id="1b41f-p101">Diese Methode kann verwendet werden, um den Inhalt des Datenstrompuffers an das zugrundeliegende Objekt (z. B. den Knoten oder die Datei, der bzw. die durch die URL dargestellt wird, bei der es sich um die Quelle des **Stream** -Objekts handelt). Diese Methode sollte aufgerufen werden, wenn Sie sicherstellen möchten, dass alle am Inhalt des **Stream** -Objekts vorgenommenen Änderungen geschrieben wurden. Bei ADO muss **Flush** in der Regel nicht aufgerufen werden, da ADO seinen Puffer in den meisten Fällen im Hintergrund leert. Die Änderungen am Inhalt eines **Stream** -Objekts werden automatisch vorgenommen und erst zwischengespeichert, wenn **Flush** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1b41f-p101">This method may be used to send the contents of the stream buffer to the underlying object (for example, the node or file represented by the URL that is the source of the **Stream** object). This method should be called when you want to ensure that all changes made to the contents of a **Stream** have been written. However, with ADO it is not usually necessary to call **Flush**, as ADO continuously flushes its buffer as much as possible in the background. Changes to the content of a **Stream** are made automatically, not cached until **Flush** is called.</span></span>

<span data-ttu-id="1b41f-112">Wenn Sie ein **Stream** -Objekt mit der [Close](close-method-ado.md)-Methode schließen, wird der Inhalt des **Stream** -Objekts automatisch geleert. Es ist nicht notwendig, **Flush** explizit unmittelbar vor **Close** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1b41f-112">Closing a **Stream** with the [Close](close-method-ado.md) method flushes the contents of a **Stream** automatically; there is no need to explicitly call **Flush** immediately before **Close**.</span></span>

