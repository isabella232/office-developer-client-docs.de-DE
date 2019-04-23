---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281901"
---
# <a name="adcpropasyncthreadpriorityenum"></a>ADCPROP\_-\_ASYNCTHREADPRIORITY-Enumeration

**Gilt für**: Access 2013, Office 2013

Gibt für ein RDS-[Recordset](recordset-object-ado.md)-Objekt die Ausführungspriorität des asynchronen Threads an, der Daten abruft.

Verwenden Sie diese Konstanten mit der dynamischen **Recordset**-Eigenschaft **Background Thread Priority**, auf die im Index für dynamische ADO-Eigenschaften verwiesen wird und die in der Dokumentation [Microsoft Cursor Service für OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) beschrieben ist.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adPriorityAboveNormal</strong></p></td>
<td><p>4</p></td>
<td><p>Legt die Priorität zwischen dem normalen Wert und dem Höchstwert fest.</p></td>
</tr>
<tr class="even">
<td><p><strong>adPriorityBelowNormal</strong></p></td>
<td><p>2</p></td>
<td><p>Legt die Priorität zwischen dem niedrigsten und dem normalen Wert fest.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityHighest</strong></p></td>
<td><p>5</p></td>
<td><p>Legt die Priorität auf den höchst möglichen Wert fest.</p></td>
</tr>
<tr class="even">
<td><p><strong>AdPriorityLowest</strong></p></td>
<td><p>1</p></td>
<td><p>Legt die Priorität auf den niedrigsten Wert fest.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPriorityNormal</strong></p></td>
<td><p>3</p></td>
<td><p>Legt die Priorität auf den normalen Wert fest.</p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a>ADO/WFC-Äquivalent

Paket: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums. AdcPropAsyncThreadPriority. ABOVENORMAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. AdcPropAsyncThreadPriority. BELOWNORMAL</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. AdcPropAsyncThreadPriority. HIGHEST</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums. AdcPropAsyncThreadPriority. NIEDRIGSTEr Wert</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums. AdcPropAsyncThreadPriority. NORMAL</p></td>
</tr>
</tbody>
</table>

