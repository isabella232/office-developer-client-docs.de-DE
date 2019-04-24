---
title: Verwenden von Seiten (Access-Desktop-Daten Bankreferenz)
TOCTitle: Using Pages
ms:assetid: 516fb7c2-c7a2-385b-83e7-2091c7283ea2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249261(v=office.15)
ms:contentKeyID: 48544817
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92d6185c3234a58ea9a84310291d0c37e0272535
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305873"
---
# <a name="using-pages"></a><span data-ttu-id="be332-102">Verwenden von Seiten</span><span class="sxs-lookup"><span data-stu-id="be332-102">Using pages</span></span>


<span data-ttu-id="be332-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be332-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be332-p101">Mit der **PageCount**-Eigenschaft bestimmen Sie die Anzahl der Datenseiten im **Recordset**-Objekt. *Seiten* sind Datensatzgruppen, deren Größe der Einstellung der **PageSize**-Eigenschaft entspricht. Selbst wenn die letzte Seite unvollständig ist, weil weniger Datensätze vorhanden sind, als für die **PageSize**-Eigenschaft angegeben ist, zählt sie als zusätzliche Seite für **PageCount**. Wenn diese Eigenschaft vom **Recordset**-Objekt nicht unterstützt wird, hat **PageCount** den Wert -1, womit **PageCount** nicht bestimmt werden kann.</span><span class="sxs-lookup"><span data-stu-id="be332-p101">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object. *Pages* are groups of records whose size equals the **PageSize** property setting. Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value. If the **Recordset** object does not support this property, **PageCount** will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="be332-p102">Mit der **PageSize** -Eigenschaft bestimmen Sie, aus wie vielen Datensätzen eine logische Datenseite besteht. Durch das Einrichten einer Seitengröße können Sie mit der **AbsolutePage** -Eigenschaft zum ersten Datensatz einer bestimmten Seite navigieren. Dies ist für Webserverszenarien hilfreich, wenn Sie dem Benutzer gestatten möchten, in den Daten zu blättern und jeweils eine bestimmte Anzahl von Datensätzen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be332-p102">Use the **PageSize** property to determine how many records make up a logical page of data. Establishing a page size allows you to use the **AbsolutePage** property to move to the first record of a particular page. This is useful in Web-server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>

<span data-ttu-id="be332-111">Diese Eigenschaft kann jederzeit festgelegt werden. Mit dem Wert dieser Eigenschaft wird die Position des ersten Datensatzes einer bestimmten Seite berechnet.</span><span class="sxs-lookup"><span data-stu-id="be332-111">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

<span data-ttu-id="be332-p103">Mit der **AbsolutePage** -Eigenschaft identifizieren Sie die Nummer der Seite, auf der sich der aktuelle Datensatz befindet. Auch in diesem Fall muss die entsprechende Funktionalität vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="be332-p103">Use the **AbsolutePage** property to identify the page number on which the current record is located. Again, the provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="be332-p104">**AbsolutePage** ist 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Legen Sie diese Eigenschaft fest, um zum ersten Datensatz einer bestimmten Seite zu navigieren. Die Gesamtanzahl der Seiten rufen Sie mit der **PageCount** -Eigenschaft ab.</span><span class="sxs-lookup"><span data-stu-id="be332-p104">**AbsolutePage** is 1-based and equals 1 when the current record is the first record in the **Recordset**. Set this property to move to the first record of a particular page. Obtain the total number of pages from the **PageCount** property.</span></span>

