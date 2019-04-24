---
title: MarshalOptions-Eigenschaft (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 22a3662d3d14dd639069fa7aa48eda6f032fd2d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289770"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="efb07-102">MarshalOptions-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="efb07-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="efb07-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="efb07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="efb07-104">Gibt die Datensätze an, die wieder zurück zum Server gemarshallt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="efb07-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="efb07-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="efb07-105">Settings And Return Values</span></span>

<span data-ttu-id="efb07-p101">Legt einen [MarshalOptionsEnum](marshaloptionsenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="efb07-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="efb07-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efb07-108">Remarks</span></span>

<span data-ttu-id="efb07-109">Bei Verwendung eines clientseitigen [Recordset-Objekts](recordset-object-ado.md)werden Datensätze, die auf dem Client geändert wurden, über eine Technik namens "Marshalling" zurück auf die mittlere Ebene oder den Webserver geschrieben, der Prozess des Packens und Sendens von Schnittstellenmethoden Parametern über den Thread oder Prozessgrenzen.</span><span class="sxs-lookup"><span data-stu-id="efb07-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="efb07-110">Das Festlegen \*\*\*\* der MarshalOptions-Eigenschaft kann die Leistung verbessern, wenn geänderte Remotedaten für die Aktualisierung zurück auf die mittlere Ebene oder den Webserver gemarshallt werden.</span><span class="sxs-lookup"><span data-stu-id="efb07-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="efb07-111">**Remote Data Service-Verwendung** Diese Eigenschaft wird nur für ein clientseitiges **Recordset**-Objekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="efb07-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

