---
title: Mode-Eigenschaft (ADO)
TOCTitle: Mode property (ADO)
ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15)
ms:contentKeyID: 48545227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f30dac303541b0f53d06eb7756739ff1add6ce0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288869"
---
# <a name="mode-property-ado"></a><span data-ttu-id="f5c6b-102">Mode-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="f5c6b-102">Mode property (ADO)</span></span>


<span data-ttu-id="f5c6b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f5c6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f5c6b-104">Es werden die verfügbaren Berechtigungen zum Ändern von Daten in einem [Connection](connection-object-ado.md)-, [Record](record-object-ado.md)- oder [Stream](stream-object-ado.md)-Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="f5c6b-104">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f5c6b-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f5c6b-105">Settings and return values</span></span>

<span data-ttu-id="f5c6b-p101">Legt einen [ConnectModeEnum](connectmodeenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert für ein **Connection**-Objekt ist **adModeUnknown**. Der Standardwert für ein **Record**-Objekt ist **adModeRead**. Der Standardwert für ein **Stream**-Objekt, das mit einer zugrunde liegenden Quelle (geöffnet mit einer URL als Quelle oder als **Stream**-Objekt eines **Record**-Objekts) verknüpft ist, lautet **adModeRead**. Der Standardwert für ein **Stream**-Objekt, das nicht mit einer zugrunde liegenden Quelle verknüpft ist (im Speicher instanziiert), lautet **adModeUnknown**.</span><span class="sxs-lookup"><span data-stu-id="f5c6b-p101">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value. The default value for a **Connection** is **adModeUnknown**. The default value for a **Record** object is **adModeRead**. The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**. The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c6b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5c6b-111">Remarks</span></span>

<span data-ttu-id="f5c6b-p102">Verwenden Sie die **Mode** -Eigenschaft, um die von einem Anbieter mit der aktuellen Verbindung verwendeten Zugriffsberechtigungen festzulegen oder zurückzugeben. Die **Mode** -Eigenschaft kann nur bei geschlossenem **Connection** -Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f5c6b-p102">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection. You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="f5c6b-p103">Wenn Sie den Zugriffsmodus bei einem **Stream** -Objekt nicht angeben, wird er von der zum Öffnen des **Stream** -Objekts verwendeten Quelle vererbt. Angenommen, Sie öffnen ein **Stream** -Objekt aus einem **Record** -Objekt, dann wird es standardmäßig in demselben Modus wie das **Record** -Objekt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f5c6b-p103">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object. For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="f5c6b-116">Die Eigenschaft ist nicht schreibgeschützt, wenn das Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="f5c6b-116">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="f5c6b-117">**Remote Data Service-Verwendung** Bei Verwendung in einem clientseitigen Connection-Objekt kann die **Mode** -Eigenschaft nur auf **adModeUnknown**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f5c6b-117">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>

