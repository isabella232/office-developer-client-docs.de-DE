---
title: Provider-Eigenschaft (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: df764aca267cab9b38760c432cd19154d6c6827f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881566"
---
# <a name="provider-property-ado"></a><span data-ttu-id="68374-102">Provider-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="68374-102">Provider property (ADO)</span></span>


<span data-ttu-id="68374-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="68374-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="68374-104">Gibt den Namen des Anbieters für ein [Connection](connection-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="68374-104">Indicates the name of the provider for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="68374-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="68374-105">Settings and return values</span></span>

<span data-ttu-id="68374-106">Legt einen **String** -Wert fest, der den Namen des Anbieters angibt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="68374-106">Sets or returns a **String** value that indicates the provider name.</span></span>

## <a name="remarks"></a><span data-ttu-id="68374-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68374-107">Remarks</span></span>

<span data-ttu-id="68374-p101">Verwenden Sie die Provider-Eigenschaft, um den Namen des Anbieters für eine Verbindung festzulegen oder zurückzugeben. Diese Eigenschaft kann mit dem Inhalt der ConnectionString-Eigenschaft oder dem Argument ConnectionString der Open-Methode festgelegt werden. Wenn Sie jedoch einen Anbieter an mehreren Stellen angeben und die Open-Methode aufrufen, kann das zu unerwarteten Ergebnissen führen. Wird kein Anbieter angegeben, gilt der Standardwert MSDASQL für diese Eigenschaft (Microsoft OLE DB-Anbieter für ODBC).</span><span class="sxs-lookup"><span data-stu-id="68374-p101">Use the **Provider** property to set or return the name of the provider for a connection. This property can also be set by the contents of the [ConnectionString](connectionstring-property-ado.md) property or the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method; however, specifying a provider in more than one place while calling the **Open** method can have unpredictable results. If no provider is specified, the property will default to MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)).</span></span>

<span data-ttu-id="68374-p102">Die **Provider** -Eigenschaft ist nicht schreibgeschützt, wenn die Verbindung geschlossen ist, und schreibgeschützt, wenn sie geöffnet ist. Die Einstellung wird erst wirksam, wenn Sie das **Connection** -Objekt öffnen oder auf die [Properties](properties-collection-ado.md)-Auflistung des **Connection** -Objekts zugreifen. Ist die Einstellung nicht gültig, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="68374-p102">The **Provider** property is read/write when the connection is closed and read-only when it is open. The setting does not take effect until you either open the **Connection** object or access the [Properties](properties-collection-ado.md) collection of the **Connection** object. If the setting is not valid, an error occurs.</span></span>

