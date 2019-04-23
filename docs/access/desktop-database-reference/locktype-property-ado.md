---
title: LockType-Eigenschaft (ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d12946a90d61a941bf5ef7d479970c8c96e074f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289843"
---
# <a name="locktype-property-ado"></a><span data-ttu-id="17043-102">LockType-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="17043-102">LockType property (ADO)</span></span>


<span data-ttu-id="17043-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17043-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17043-104">Gibt den Typ der Sperren an, die bei der Bearbeitung auf Datensätze angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="17043-104">Indicates the type of locks placed on records during editing.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="17043-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="17043-105">Settings and return values</span></span>

<span data-ttu-id="17043-106">Legt einen [LockTypeEnum](locktypeenum.md)-Wert fest oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="17043-106">Sets or returns a [LockTypeEnum](locktypeenum.md) value.</span></span> <span data-ttu-id="17043-107">Der Standardwert ist **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="17043-107">The default value is **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="17043-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17043-108">Remarks</span></span>

<span data-ttu-id="17043-p102">Legen Sie die **LockType** -Eigenschaft fest, bevor Sie ein [Recordset](recordset-object-ado.md) öffnen, und geben Sie den Sperrtyp an, den der Anbieter beim Öffnen verwenden soll. Lesen Sie die Eigenschaft, um den Sperrtyp zu ermitteln, der bei einem geöffneten **Recordset** -Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17043-p102">Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="17043-p103">Anbieter unterstützen möglicherweise nicht alle Sperrtypen. Falls ein Anbieter die angeforderte **LockType** -Einstellung nicht unterstützt, wird der Sperrtyp ausgetauscht. Wenn Sie die Sperrfunktionalität ermitteln möchten, die tatsächlich für ein **Recordset** -Objekt verfügbar ist, verwenden Sie die [Supports](supports-method-ado.md)-Methode mit **adUpdate** und **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="17043-p103">Providers may not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="17043-p104">Die Einstellung **adLockPessimistic** wird nicht unterstützt, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist. Wurde ein nicht unterstützter Wert festgelegt, tritt kein Fehler auf. Stattdessen wird der nächstliegende unterstützte **LockType** -Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="17043-p104">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="17043-116">Die **LockType** -Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset** -Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="17043-116">The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="17043-117">**Remote Data Service-Verwendung** Bei Verwendung in einem clientseitigen Recordset-Objekt kann \*\*\*\* die LockType-Eigenschaft nur auf **adLockBatchOptimistic**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="17043-117">**Remote Data Service Usage**When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**.</span></span>

