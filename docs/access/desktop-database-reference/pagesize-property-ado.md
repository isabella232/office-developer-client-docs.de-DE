---
title: PageSize-Eigenschaft (ADO)
TOCTitle: PageSize Property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89b28e382f1597ff6466aa323565eaf2ff068605
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473045"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="fe384-102">PageSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="fe384-102">PageSize Property (ADO)</span></span>


<span data-ttu-id="fe384-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe384-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fe384-104">Gibt an, aus wie vielen Datensätze eine Seite im [Recordset](recordset-object-ado.md) besteht.</span><span class="sxs-lookup"><span data-stu-id="fe384-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="fe384-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="fe384-105">Settings and Return Values</span></span>

<span data-ttu-id="fe384-p101">Legt einen Long-Wert fest, der angibt, wie viele Datensätze sich auf einer Seite befinden. Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="fe384-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe384-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fe384-108">Remarks</span></span>

<span data-ttu-id="fe384-p102">Mit der **PageSize** -Eigenschaft bestimmen Sie, aus wie vielen Datensätzen eine logische Datenseite besteht. Durch das Einrichten einer Seitengröße können Sie mit der [AbsolutePage](absolutepage-property-ado.md)-Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren. Dies ist für Webserverszenarien hilfreich, wenn Sie dem Benutzer gestatten möchten, in den Daten zu blättern und jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fe384-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page. This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="fe384-112">Diese Eigenschaft kann jederzeit festgelegt werden. Mit ihrem Wert wird berechnet, wo sich der erste Datensatz auf einer bestimmten Seite befindet.</span><span class="sxs-lookup"><span data-stu-id="fe384-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

