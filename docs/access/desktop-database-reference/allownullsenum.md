---
title: AllowNullsEnum (Access PC-Datenbank-Referenz)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c4c44771258cd94700bfb2902cf8bdad47a2d712
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860140"
---
# <a name="allownullsenum"></a><span data-ttu-id="5394e-102">AllowNullsEnum</span><span class="sxs-lookup"><span data-stu-id="5394e-102">AllowNullsEnum</span></span>

<span data-ttu-id="5394e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5394e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5394e-104">Gibt an, ob Datensätze mit Nullwerten indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5394e-104">Specifies whether records with null values are indexed.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5394e-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="5394e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5394e-106">Wert</span><span class="sxs-lookup"><span data-stu-id="5394e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5394e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5394e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5394e-108"><strong>adIndexNullsAllow</strong></span><span class="sxs-lookup"><span data-stu-id="5394e-108"><strong>adIndexNullsAllow</strong></span></span></p></td>
<td><p><span data-ttu-id="5394e-109">0</span><span class="sxs-lookup"><span data-stu-id="5394e-109">0</span></span></p></td>
<td><p><span data-ttu-id="5394e-p101">Der Index lässt Einträge mit nullwertigen Schlüsselspalten zu. Wenn ein Nullwert in eine Schlüsselspalte eingegeben wird, wird der Eintrag in den Index eingefügt.</span><span class="sxs-lookup"><span data-stu-id="5394e-p101">The index does allow entries in which the key columns are null. If a null value is entered in a key column, the entry is inserted into the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5394e-112"><strong>adIndexNullsDisallow</strong></span><span class="sxs-lookup"><span data-stu-id="5394e-112"><strong>adIndexNullsDisallow</strong></span></span></p></td>
<td><p><span data-ttu-id="5394e-113">1</span><span class="sxs-lookup"><span data-stu-id="5394e-113">1</span></span></p></td>
<td><p><span data-ttu-id="5394e-p102">Standardeinstellung. Der Index lässt keine Einträge mit nullwertigen Schlüsselspalten zu. Wenn ein Nullwert in eine Schlüsselspalte eingegeben wird, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="5394e-p102">Default. The index does not allow entries in which the key columns are null. If a null value is entered in a key column, an error will occur.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5394e-117"><strong>adIndexNullsIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="5394e-117"><strong>adIndexNullsIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="5394e-118">2</span><span class="sxs-lookup"><span data-stu-id="5394e-118">2</span></span></p></td>
<td><p><span data-ttu-id="5394e-p103">Der Index fügt keine Einträge mit nullwertigen Schlüsselspalten ein. Wenn ein Nullwert in eine Schlüsselspalte eingegeben wird, wird der Eintrag ignoriert, und es tritt kein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="5394e-p103">The index does not insert entries containing null keys. If a null value is entered in a key column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5394e-121"><strong>adIndexNullsIgnoreAny</strong></span><span class="sxs-lookup"><span data-stu-id="5394e-121"><strong>adIndexNullsIgnoreAny</strong></span></span></p></td>
<td><p><span data-ttu-id="5394e-122">4</span><span class="sxs-lookup"><span data-stu-id="5394e-122">4</span></span></p></td>
<td><p><span data-ttu-id="5394e-p104">Der Index fügt keine Einträge mit einer nullwertigen Schlüsselspalte ein. Bei einem Index mit einem mehrspaltigen Schlüssel wird der Eintrag ignoriert und kein Fehler ausgelöst, wenn ein Nullwert in eine Spalte eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5394e-p104">The index does not insert entries where some key column has a null value. For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
</tbody>
</table>

