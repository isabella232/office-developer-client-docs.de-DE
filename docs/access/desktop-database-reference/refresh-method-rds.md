---
title: Refresh-Methode (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d49b91f129a0661c5c81243bb405de9088b1e06d
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950118"
---
# <a name="refresh-method-rds"></a><span data-ttu-id="89723-102">Refresh-Methode (RDS)</span><span class="sxs-lookup"><span data-stu-id="89723-102">Refresh method (RDS)</span></span>

<span data-ttu-id="89723-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89723-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89723-104">Fragt die in der [Connect](connect-property-rds.md)-Eigenschaft angegebene Datenquelle erneut ab und aktualisiert die Abfrageergebnisse.</span><span class="sxs-lookup"><span data-stu-id="89723-104">Requeries the data source specified in the [Connect](connect-property-rds.md) property and updates the query results.</span></span>

## <a name="syntax"></a><span data-ttu-id="89723-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="89723-105">Syntax</span></span>

<span data-ttu-id="89723-106">*DataControl*. Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="89723-106">*DataControl*.Refresh</span></span>

## <a name="parameters"></a><span data-ttu-id="89723-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="89723-107">Parameters</span></span>

|<span data-ttu-id="89723-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="89723-108">Parameter</span></span>|<span data-ttu-id="89723-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89723-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="89723-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="89723-110">*DataControl*</span></span> |<span data-ttu-id="89723-111">Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="89723-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="89723-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89723-112">Remarks</span></span>

<span data-ttu-id="89723-p101">Bevor Sie die [Refresh](connect-property-rds.md) -Methode verwenden, müssen Sie die Eigenschaften [Connect](server-property-rds.md), [Server](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) und **SQL** festlegen. Alle datengebundenen Steuerelemente auf dem Formular, das einem **RDS.DataControl** -Objekt zugeordnet ist, geben die neue Datensatzgruppe wieder. Ein bereits vorhandenes [Recordset](recordset-object-ado.md)-Objekt wird freigegeben, und alle nicht gespeicherten Änderungen werden verworfen. Mithilfe der **Refresh** -Methode wird der erste Datensatz automatisch zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="89723-p101">You must set the [Connect](connect-property-rds.md), [Server](server-property-rds.md), and [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) properties before you use the **Refresh** method. All data-bound controls on the form associated with an **RDS.DataControl** object will reflect the new set of records. Any pre-existing [Recordset](recordset-object-ado.md) object is released, and any unsaved changes are discarded. The **Refresh** method automatically makes the first record the current record.</span></span>

<span data-ttu-id="89723-p102">Es wird empfohlen, die **Refresh** -Methode regelmäßig aufzurufen, wenn Sie mit Daten arbeiten. Wenn Sie Daten abrufen und diese eine Weile auf dem Clientcomputer speichern, sind diese wahrscheinlich nach kurzer Zeit nicht mehr aktuell. Es kann vorkommen, dass von Ihnen vorgenommene Änderungen fehlschlagen, da der Datensatz möglicherweise von einer anderen Person geändert und vor Ihnen übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="89723-p102">It's a good idea to call the **Refresh** method periodically when you work with data. If you retrieve data, and then leave it on your client machine for a while, it is likely to become out of date. It's possible that any changes you make will fail, because someone else might have changed the record and submitted changes before you.</span></span>

