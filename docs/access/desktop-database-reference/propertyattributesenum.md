---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8f01efcc98ed12858712c28f080fb066d3dc1b41
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473928"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="7bb58-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="7bb58-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="7bb58-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bb58-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7bb58-104">Gibt die Attribute eines [Property](property-object-ado.md)-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="7bb58-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bb58-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="7bb58-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7bb58-106">Wert</span><span class="sxs-lookup"><span data-stu-id="7bb58-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7bb58-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bb58-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bb58-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="7bb58-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb58-109">0</span><span class="sxs-lookup"><span data-stu-id="7bb58-109">0</span></span></p></td>
<td><p><span data-ttu-id="7bb58-110">Gibt an, dass die Eigenschaft vom Anbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7bb58-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb58-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="7bb58-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb58-112">1</span><span class="sxs-lookup"><span data-stu-id="7bb58-112">1</span></span></p></td>
<td><p><span data-ttu-id="7bb58-113">Gibt an, dass der Benutzer einen Wert für diese Eigenschaft angeben muss, bevor die Datenquelle initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7bb58-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb58-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="7bb58-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb58-115">2</span><span class="sxs-lookup"><span data-stu-id="7bb58-115">2</span></span></p></td>
<td><p><span data-ttu-id="7bb58-116">Gibt an, dass der Benutzer keinen Wert für diese Eigenschaft angeben muss, bevor die Datenquelle initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7bb58-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb58-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="7bb58-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb58-118">512</span><span class="sxs-lookup"><span data-stu-id="7bb58-118">512</span></span></p></td>
<td><p><span data-ttu-id="7bb58-119">Gibt an, dass der Benutzer die Eigenschaft lesen kann.</span><span class="sxs-lookup"><span data-stu-id="7bb58-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb58-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="7bb58-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="7bb58-121">1024</span><span class="sxs-lookup"><span data-stu-id="7bb58-121">1024</span></span></p></td>
<td><p><span data-ttu-id="7bb58-122">Gibt an, dass der Benutzer die Eigenschaft festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="7bb58-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7bb58-123">**ADO/WFC-Entsprechung**</span><span class="sxs-lookup"><span data-stu-id="7bb58-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="7bb58-124">Paket: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="7bb58-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bb58-125">Konstante</span><span class="sxs-lookup"><span data-stu-id="7bb58-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bb58-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="7bb58-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb58-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="7bb58-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb58-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="7bb58-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bb58-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="7bb58-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bb58-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="7bb58-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

