---
title: PageSize-Eigenschaft (ADO)
TOCTitle: PageSize property (ADO)
ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15)
ms:contentKeyID: 48548079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9365acb13820f898c053d4c90fc252bfd3b228c4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709551"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="49de3-102">PageSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="49de3-102">PageSize property (ADO)</span></span>


<span data-ttu-id="49de3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49de3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49de3-104">Gibt an, aus wie vielen Datensätze eine Seite im [Recordset](recordset-object-ado.md) besteht.</span><span class="sxs-lookup"><span data-stu-id="49de3-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="49de3-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="49de3-105">Settings and return values</span></span>

<span data-ttu-id="49de3-p101">Legt einen Long-Wert fest, der angibt, wie viele Datensätze sich auf einer Seite befinden. Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="49de3-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="49de3-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="49de3-108">Remarks</span></span>

<span data-ttu-id="49de3-109">Mit der **PageSize** -Eigenschaft bestimmen Sie, aus wie vielen Datensätzen eine logische Datenseite besteht.</span><span class="sxs-lookup"><span data-stu-id="49de3-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="49de3-110">Durch das Einrichten einer Seitengröße können Sie mit der [AbsolutePage](absolutepage-property-ado.md)-Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="49de3-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="49de3-111">Dies ist nützlich in Szenarien, Web Server, wenn Sie den Benutzer zur Seite durch Daten sowie zulassen, jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="49de3-111">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="49de3-112">Diese Eigenschaft kann jederzeit festgelegt werden. Mit ihrem Wert wird berechnet, wo sich der erste Datensatz auf einer bestimmten Seite befindet.</span><span class="sxs-lookup"><span data-stu-id="49de3-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

