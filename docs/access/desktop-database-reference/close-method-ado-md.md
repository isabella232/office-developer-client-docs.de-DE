---
title: Close-Methode (ADO MD)
TOCTitle: Close Method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28c5ff23470015c9b40c996a1eb5b60f74766da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888790"
---
# <a name="close-method-ado-md"></a><span data-ttu-id="0723d-102">Close-Methode (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="0723d-102">Close Method (ADO MD)</span></span>


<span data-ttu-id="0723d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0723d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0723d-104">Schließt eine geöffnete Zellmenge.</span><span class="sxs-lookup"><span data-stu-id="0723d-104">Closes an open cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="0723d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0723d-105">Syntax</span></span>

<span data-ttu-id="0723d-106">*Zellmenge*. Schließen Sie</span><span class="sxs-lookup"><span data-stu-id="0723d-106">*Cellset*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="0723d-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0723d-107">Remarks</span></span>

<span data-ttu-id="0723d-p101">Durch das Verwenden der **Close** -Methode zum Schließen eines [Cellset](cellset-object-ado-md.md)-Objekts werden die verbundenen Daten freigegeben, einschließlich der Daten in allen verknüpften [Cell](cell-object-ado-md.md)-, [Axis](axis-object-ado-md.md)-, [Position](position-object-ado-md.md)- oder [Member](member-object-ado-md.md)-Objekten. Durch das Schließen eines **Cellset** -Objekts wird dieses nicht aus dem Speicher gelöscht. Sie können die Eigenschafteneinstellungen des Objekts ändern und es später erneut öffnen. Um ein Objekt vollständig aus dem Speicher zu entfernen, legen Sie die Objektvariable auf **Nothing** fest.</span><span class="sxs-lookup"><span data-stu-id="0723d-p101">Using the **Close** method to close a [Cellset](cellset-object-ado-md.md) object will release the associated data, including data in any related [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md), or [Member](member-object-ado-md.md) objects. Closing a **Cellset** does not remove it from memory; you can change its property settings and open it again later. To completely eliminate an object from memory, set the object variable to **Nothing**.</span></span>

<span data-ttu-id="0723d-p102">Sie können die [Open](open-method-ado-md.md)-Methode später aufrufen, um das **Cellset** -Objekt später mithilfe derselben oder einer anderen Quellzeichenfolge erneut zu öffnen. Während das **Cellset** -Objekt geschlossen ist, tritt ein Fehler auf, wenn Eigenschaften abgerufen oder Methoden aufgerufen werden, die auf die zugrunde liegenden Daten oder Metadaten verweisen.</span><span class="sxs-lookup"><span data-stu-id="0723d-p102">You can later call the [Open](open-method-ado-md.md) method to reopen the **Cellset** using the same or another source string. While the **Cellset** object is closed, retrieving any properties or calling any methods that reference the underlying data or metadata generates an error.</span></span>

