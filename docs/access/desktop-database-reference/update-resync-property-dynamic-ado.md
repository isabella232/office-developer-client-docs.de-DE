---
title: Update Resync (dynamische Eigenschaft) (ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4eea391e99202eeb075d73daa1034dff2042e49
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604421"
---
# <a name="update-resync-property--dynamic-ado"></a><span data-ttu-id="f8984-102">Update Resync (dynamische Eigenschaft) (ADO)</span><span class="sxs-lookup"><span data-stu-id="f8984-102">Update Resync Property--Dynamic (ADO)</span></span>


<span data-ttu-id="f8984-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8984-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f8984-104">Gibt an, ob auf die [UpdateBatch](updatebatch-method-ado.md)-Methode ein impliziter Vorgang mit einer [Resync](resync-method-ado.md)-Methode folgt. Wenn dies der Fall ist, wird der Bereich des Vorgangs angegeben.</span><span class="sxs-lookup"><span data-stu-id="f8984-104">Specifies whether the [UpdateBatch](updatebatch-method-ado.md) method is followed by an implicit [Resync](resync-method-ado.md) method operation, and if so, the scope of that operation.</span></span>

<span data-ttu-id="f8984-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="f8984-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="f8984-106">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f8984-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="f8984-107">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f8984-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="f8984-108">master</span><span class="sxs-lookup"><span data-stu-id="f8984-108">master</span></span>

<span data-ttu-id="f8984-109">Legt fest oder gibt mindestens eines der [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) Werte.</span><span class="sxs-lookup"><span data-stu-id="f8984-109">Sets or returns one or more of the [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8984-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8984-110">Remarks</span></span>

<span data-ttu-id="f8984-111">Die Werte der ADCPROP\_UPDATERESYNC\_ENUM kann kombiniert werden, und abgesehen vom Wert AdResyncAll, der bereits die Kombination der restlichen Werte darstellt.</span><span class="sxs-lookup"><span data-stu-id="f8984-111">The values of ADCPROP\_UPDATERESYNC\_ENUM may be combined, except for adResyncAll which already represents the combination of the rest of the values.</span></span>

<span data-ttu-id="f8984-112">Mit der **adResyncConflicts** -Konstante werden die Neusynchronisierungswerte als zugrunde liegende Werte gespeichert, aber ausstehende Änderungen werden nicht außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="f8984-112">The constant **adResyncConflicts** stores the resync values as underlying values, but does not override pending changes.</span></span>

<span data-ttu-id="f8984-113">**Update Resync** ist eine dynamische Eigenschaft, die an die [Properties](recordset-object-ado.md)-Auflistung des [Recordset](properties-collection-ado.md)-Objekts angefügt wird, wenn die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f8984-113">**Update Resync** is a dynamic property appended to the [Recordset](recordset-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

