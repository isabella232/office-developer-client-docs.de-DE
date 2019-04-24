---
title: DataSource-Eigenschaft (ADO)
TOCTitle: DataSource property (ADO)
ms:assetid: 5c5d6c9b-b7d4-45a5-0f6a-a5580a74361e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249325(v=office.15)
ms:contentKeyID: 48545087
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0dec30715d1eb4e31d7490db4cedd015ecf3c040
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294470"
---
# <a name="datasource-property-ado"></a><span data-ttu-id="dd3de-102">DataSource-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="dd3de-102">DataSource property (ADO)</span></span>


<span data-ttu-id="dd3de-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd3de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd3de-104">Gibt ein Objekt an, das als [Recordset](recordset-object-ado.md)-Objekt darzustellende Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="dd3de-104">Indicates an object that contains data to be represented as a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd3de-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dd3de-105">Remarks</span></span>

<span data-ttu-id="dd3de-p101">Mithilfe dieser Eigenschaft werden datengebundene Steuerelemente mit der Datenumgebung erstellt. Die Datenumgebung verwaltet Datensammlungen (Datenquellen), die benannte Objekte (*Datenelemente*) enthalten und als **Recordset**-Objekt dargestellt werden.\*\*</span><span class="sxs-lookup"><span data-stu-id="dd3de-p101">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a **Recordset** object *.*</span></span>

<span data-ttu-id="dd3de-108">Die Eigenschaften [DataMember](datamember-property-ado.md) und **DataSource** müssen in Kombination verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd3de-108">The [DataMember](datamember-property-ado.md) and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="dd3de-109">Das Objekt, auf das verwiesen wird, muss die **IDataSource** -Schnittstelle implementieren und eine **IRowset** -Schnittstelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="dd3de-109">The object referenced must implement the **IDataSource** interface and must contain an **IRowset** interface.</span></span>

<span data-ttu-id="dd3de-110">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="dd3de-110">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
