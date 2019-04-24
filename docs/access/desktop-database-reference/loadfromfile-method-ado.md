---
title: LoadFrom-Methode (ADO)
TOCTitle: LoadFromFile method (ADO)
ms:assetid: 33fd543f-bd24-9199-7540-2889b69221c8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249107(v=office.15)
ms:contentKeyID: 48544123
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9316bc4302a559fa44082a0576595707157e9d64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289885"
---
# <a name="loadfromfile-method-ado"></a><span data-ttu-id="c48aa-102">LoadFrom-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="c48aa-102">LoadFromFile method (ADO)</span></span>

<span data-ttu-id="c48aa-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c48aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c48aa-104">Lädt den Inhalt einer vorhandenen Datei in ein [Stream](stream-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c48aa-104">Loads the contents of an existing file into a [Stream](stream-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c48aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c48aa-105">Syntax</span></span>

<span data-ttu-id="c48aa-106">*Stream*. *Dateinamen* für loadfromdatei</span><span class="sxs-lookup"><span data-stu-id="c48aa-106">*Stream*.LoadFromFile *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="c48aa-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c48aa-107">Parameters</span></span>

|<span data-ttu-id="c48aa-108">Name</span><span class="sxs-lookup"><span data-stu-id="c48aa-108">Name</span></span> |<span data-ttu-id="c48aa-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c48aa-109">Description</span></span>|
|:----|:----------|
|<span data-ttu-id="c48aa-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="c48aa-110">*FileName*</span></span> |<span data-ttu-id="c48aa-p101">Ein **String**-Wert, der den Namen der in das **Stream**-Objekt zu ladenden Datei enthält. *FileName* kann einen beliebigen gültigen Pfad und Namen im UNC-Format enthalten. Wenn die angegebene Datei nicht vorhanden ist, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="c48aa-p101">A **String** value that contains the name of a file to be loaded into the **Stream**. *FileName* can contain any valid path and name in UNC format. If the specified file does not exist, a run-time error occurs.</span></span>|

## <a name="remarks"></a><span data-ttu-id="c48aa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c48aa-114">Remarks</span></span>

<span data-ttu-id="c48aa-p102">Diese Methode kann verwendet werden, um den Inhalt einer lokalen Datei in ein **Stream**-Objekt zu laden (z. B. zum Hochladen des Inhalts einer lokalen Datei auf einen Server).</span><span class="sxs-lookup"><span data-stu-id="c48aa-p102">This method may be used to load the contents of a local file into a **Stream** object. This may be used to upload the contents of a local file to a server.</span></span>

<span data-ttu-id="c48aa-p103">Das **Stream** -Objekt muss vor dem Aufrufen von **LoadFromFile** bereits geöffnet sein. Diese Methode ändert die Bindung des **Stream** -Objekts nicht. Es bleibt an das Objekt gebunden, das durch die URL oder den **Record** angegeben wird, mit der bzw. dem das **Stream** -Objekt ursprünglich geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="c48aa-p103">The **Stream** object must be already open before calling **LoadFromFile**. This method does not change the binding of the **Stream** object; it will still be bound to the object specified by the URL or **Record** with which the **Stream** was originally opened.</span></span>

<span data-ttu-id="c48aa-p104">**LoadFromFile** überschreibt den aktuellen Inhalt des **Stream** -Objekts mit den aus der Datei gelesenen Daten. Alle im **Stream** -Objekt vorhandenen Bytes werden mit dem Inhalt der Datei überschrieben. Alle zuvor vorhandenen und verbleibenden Bytes, die auf das von [LoadFromFile](eos-property-ado.md) erstellte **EOS** folgen, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="c48aa-p104">**LoadFromFile** overwrites the current contents of the **Stream** object with data read from the file. Any existing bytes in the **Stream** are overwritten by the contents of the file. Any previously existing and remaining bytes following the [EOS](eos-property-ado.md) created by **LoadFromFile**, are truncated.</span></span>

<span data-ttu-id="c48aa-122">Nach einem Aufruf von **loadfromdatei**wird die aktuelle Position auf den Anfang des **Streams** festgelegt ([Position](position-property-ado.md) ist 0).</span><span class="sxs-lookup"><span data-stu-id="c48aa-122">After a call to **LoadFromFile**, the current position is set to the beginning of the **Stream** ([Position](position-property-ado.md) is 0).</span></span>

<span data-ttu-id="c48aa-123">Da dem Anfang des Datenstroms zur Verschlüsselung zwei Bytes hinzugefügt werden können, entspricht die Größe des Datenstroms möglicherweise nicht genau der Größe der Datei, aus der dieser geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="c48aa-123">Because 2 bytes may be added to the beginning of the stream for encoding, the size of the stream may not exactly match the size of the file from which it was loaded.</span></span>

