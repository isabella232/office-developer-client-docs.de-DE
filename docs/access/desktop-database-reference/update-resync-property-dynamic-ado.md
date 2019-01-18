---
title: Update Resync dynamische-Eigenschaft (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702026"
---
# <a name="update-resync-dynamic-property-ado"></a><span data-ttu-id="4745f-102">Update Resync dynamische-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="4745f-102">Update Resync dynamic property (ADO)</span></span>


<span data-ttu-id="4745f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4745f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4745f-104">Gibt an, ob auf die [UpdateBatch](updatebatch-method-ado.md)-Methode ein impliziter Vorgang mit einer [Resync](resync-method-ado.md)-Methode folgt. Wenn dies der Fall ist, wird der Bereich des Vorgangs angegeben.</span><span class="sxs-lookup"><span data-stu-id="4745f-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4745f-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4745f-105">Settings and return values</span></span>

<span data-ttu-id="4745f-106">Legt fest oder gibt mindestens eines der [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) Werte.</span><span class="sxs-lookup"><span data-stu-id="4745f-106">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4745f-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4745f-107">Remarks</span></span>

<span data-ttu-id="4745f-108">Die Werte der ADCPROP\_UPDATERESYNC\_ENUM kann kombiniert werden, und abgesehen vom Wert AdResyncAll, der bereits die Kombination der restlichen Werte darstellt.</span><span class="sxs-lookup"><span data-stu-id="4745f-108">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="4745f-109">Mit der **adResyncConflicts** -Konstante werden die Neusynchronisierungswerte als zugrunde liegende Werte gespeichert, aber ausstehende Änderungen werden nicht außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="4745f-109">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="4745f-110">**Update Resync** ist eine dynamische Eigenschaft, die an die [Properties](recordset-object-ado.md)-Auflistung des [Recordset](properties-collection-ado.md)-Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4745f-110">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

