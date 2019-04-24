---
title: StayInSync-Eigenschaft (ADO)
TOCTitle: StayInSync property (ADO)
ms:assetid: 02c95c10-4032-14e1-e506-f334a8787142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248792(v=office.15)
ms:contentKeyID: 48542966
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfc9ef5229fe230ad0c83ebde7a887e0fac0c233
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308491"
---
# <a name="stayinsync-property-ado"></a><span data-ttu-id="8c839-102">StayInSync-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8c839-102">StayInSync property (ADO)</span></span>


<span data-ttu-id="8c839-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c839-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c839-104">Gibt in einem hierarchischen [Recordset](recordset-object-ado.md) -Objekt an, ob sich der Verweis auf die zugrunde liegenden untergeordneten Datensätze (also das *Kapitel*) ändert, wenn die übergeordnete Zeilenposition geändert wird.</span><span class="sxs-lookup"><span data-stu-id="8c839-104">Indicates, in a hierarchical [Recordset](recordset-object-ado.md) object, whether the reference to the underlying child records (that is, the *chapter*) changes when the parent row position changes.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8c839-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8c839-105">Settings and return values</span></span>

<span data-ttu-id="8c839-p101">Legt einen **Boolean**-Wert fest oder gibt den Wert zurück. Der Standardwert lautet **True**. Wenn **True** festgelegt ist, wird das Kapitel bei einer Änderung der Zeilenposition des übergeordneten **Recordset**-Objekts aktualisiert. Ist **False** festgelegt, verweist das Kapitel weiterhin auf Daten im vorherigen Kapitel, auch wenn sich die Zeilenposition des übergeordneten **Recordset**-Objekts geändert hat.</span><span class="sxs-lookup"><span data-stu-id="8c839-p101">Sets or returns a **Boolean** value. The default value is **True**. If **True**, the chapter will be updated if the parent **Recordset** object changes row position; if **False**, the chapter will continue to refer to data in the previous chapter even though the parent **Recordset** object has changed row position.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c839-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8c839-109">Remarks</span></span>

<span data-ttu-id="8c839-p102">Diese Eigenschaft gilt für hierarchische Recordsets wie diejenigen, die vom [Microsoft Data Shaping Dienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) unterstützt werden. Die Eigenschaft muss für das übergeordnete **Recordset**-Objekt festgelegt werden, bevor das untergeordnete **Recordset**-Objekt abgerufen wird. Das Navigieren in hierarchischen Recordsets wird mit dieser Eigenschaft vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="8c839-p102">This property applies to hierarchical Recordsets, such as those supported by the [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), and must be set on the parent **Recordset** before the child **Recordset** is retrieved. This property simplifies navigating hierarchical recordsets.</span></span>

