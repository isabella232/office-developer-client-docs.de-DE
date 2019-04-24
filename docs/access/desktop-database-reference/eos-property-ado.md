---
title: EOS-Eigenschaft (ADO-Access-Desktop-Daten Bankreferenz))
TOCTitle: EOS property (ADO)
ms:assetid: 97cd23ef-cca8-4dcc-2641-082a0e1b853c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249676(v=office.15)
ms:contentKeyID: 48546474
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a35503fb0ad320e82ed385c7014b2a18de586064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293525"
---
# <a name="eos-property-ado"></a><span data-ttu-id="96828-102">EOS-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="96828-102">EOS property (ADO)</span></span>


<span data-ttu-id="96828-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96828-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96828-104">Es wird angegeben, ob sich die aktuelle Position am Ende des Datenstroms befindet.</span><span class="sxs-lookup"><span data-stu-id="96828-104">Indicates whether the current position is at the end of the stream.</span></span>

## <a name="return-values"></a><span data-ttu-id="96828-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="96828-105">Return values</span></span>

<span data-ttu-id="96828-p101">Gibt einen Wert vom Datentyp **Boolean** zurück, der angibt, ob sich die aktuelle Position am Ende des Datenstroms befindet. **EOS** gibt **True** zurück, wenn keine Bytes mehr im Datenstrom vorhanden sind. Wenn auf die aktuelle Position noch Bytes folgen, wird **False** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="96828-p101">Returns a **Boolean** value that indicates whether the current position is at the end of the stream. **EOS** returns **True** if there are no more bytes in the stream; it returns **False** if there are more bytes following the current position.</span></span>

<span data-ttu-id="96828-p102">Verwenden Sie die [SetEOS](seteos-method-ado.md)-Methode, um das Ende der Datenstromposition festzulegen. Mithilfe der [Position](position-property-ado.md)-Eigenschaft bestimmen Sie die aktuelle Position.</span><span class="sxs-lookup"><span data-stu-id="96828-p102">To set the end of stream position, use the [SetEOS](seteos-method-ado.md) method. To determine the current position, use the [Position](position-property-ado.md) property.</span></span>

