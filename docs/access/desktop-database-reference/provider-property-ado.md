---
title: Provider-Eigenschaft (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e640fb6131919cbdf88fbbf8229c62d0e2e4e13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301134"
---
# <a name="provider-property-ado"></a><span data-ttu-id="3d08b-102">Provider-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="3d08b-102">Provider property (ADO)</span></span>


<span data-ttu-id="3d08b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d08b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d08b-104">Gibt den Namen des Anbieters für ein [Connection](connection-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3d08b-104">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3d08b-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3d08b-105">Settings and return values</span></span>

<span data-ttu-id="3d08b-106">Legt einen **String**-Wert fest, der den Namen des Anbieters angibt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3d08b-106">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d08b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d08b-107">Remarks</span></span>

<span data-ttu-id="3d08b-108">Use the **Provider** property to set or return the name of the provider for a connection.</span><span class="sxs-lookup"><span data-stu-id="3d08b-108">Use the **Provider** property to set or return the name of the provider for a connection.</span></span> <span data-ttu-id="3d08b-109">Diese Eigenschaft kann auch durch den Inhalt der [ConnectionString](connectionstring-property-ado.md) -Eigenschaft oder des *ConnectionString* -Arguments der [Open](open-method-ado-connection.md) -Methode festgelegt werden. die Angabe eines Anbieters an mehreren Stellen beim Aufrufen der **Open** -Methode kann jedoch zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="3d08b-109">This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results.</span></span> <span data-ttu-id="3d08b-110">Wenn kein Anbieter angegeben wird, wird die Eigenschaft standardmäßig auf MSDASQL ([Microsoft OLE DB-Anbieter für ODBC](microsoft-ole-db-provider-for-odbc.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d08b-110">If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="3d08b-p102">Die **Provider**-Eigenschaft ist nicht schreibgeschützt, wenn die Verbindung geschlossen ist, und schreibgeschützt, wenn sie geöffnet ist. Die Einstellung wird erst wirksam, wenn Sie das **Connection**-Objekt öffnen oder auf die [Properties](properties-collection-ado.md)-Auflistung des **Connection**-Objekts zugreifen. Ist die Einstellung nicht gültig, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3d08b-p102">The **Provider** property is read/write when the connection is closed and read-only when it is open. The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object. If the setting is not valid, an error occurs.</span></span>

