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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288133"
---
# <a name="pagesize-property-ado"></a><span data-ttu-id="d21c0-102">PageSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="d21c0-102">PageSize property (ADO)</span></span>


<span data-ttu-id="d21c0-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d21c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d21c0-104">Gibt an, aus wie vielen Datensätze eine Seite im [Recordset](recordset-object-ado.md) besteht.</span><span class="sxs-lookup"><span data-stu-id="d21c0-104">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d21c0-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d21c0-105">Settings and return values</span></span>

<span data-ttu-id="d21c0-106">Sets or returns a **Long** value that indicates how many records are on a page.</span><span class="sxs-lookup"><span data-stu-id="d21c0-106">Sets or returns a **Long** value that indicates how many records are on a page.</span></span> <span data-ttu-id="d21c0-107">The default is 10.</span><span class="sxs-lookup"><span data-stu-id="d21c0-107">The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="d21c0-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d21c0-108">Remarks</span></span>

<span data-ttu-id="d21c0-109">Mit der **PageSize**-Eigenschaft bestimmen Sie, aus wie vielen Datensätzen eine logische Datenseite besteht.</span><span class="sxs-lookup"><span data-stu-id="d21c0-109">Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="d21c0-110">Durch das Einrichten einer Seitengröße können Sie mit der [AbsolutePage](absolutepage-property-ado.md)-Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren.</span><span class="sxs-lookup"><span data-stu-id="d21c0-110">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="d21c0-111">Dies ist in Webserver Szenarios hilfreich, wenn Sie dem Benutzer erlauben möchten, über Daten zu blättern und gleichzeitig eine bestimmte Anzahl von Datensätzen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d21c0-111">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="d21c0-112">Diese Eigenschaft kann jederzeit festgelegt werden. Mit dem Wert dieser Eigenschaft wird die Position des ersten Datensatzes einer bestimmten Seite berechnet.</span><span class="sxs-lookup"><span data-stu-id="d21c0-112">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

