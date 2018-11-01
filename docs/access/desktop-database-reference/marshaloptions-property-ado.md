---
title: MarshalOptions-Eigenschaft (ADO)
TOCTitle: MarshalOptions property (ADO)
ms:assetid: dc9c4e94-0725-210d-8251-079054541142
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250118(v=office.15)
ms:contentKeyID: 48548143
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f5983b7794677b5cc584c541289069acf282d9f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883211"
---
# <a name="marshaloptions-property-ado"></a><span data-ttu-id="1d8e1-102">MarshalOptions-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="1d8e1-102">MarshalOptions property (ADO)</span></span>


<span data-ttu-id="1d8e1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d8e1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d8e1-104">Gibt die Datensätze an, die wieder zurück zum Server gemarshallt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-104">Indicates which records are to be marshaled back to the server.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1d8e1-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1d8e1-105">Settings And Return Values</span></span>

<span data-ttu-id="1d8e1-p101">Legt einen [MarshalOptionsEnum](marshaloptionsenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **adMarshalAll**.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-p101">Sets or returns a [MarshalOptionsEnum](marshaloptionsenum.md) value. The default value is **adMarshalAll**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d8e1-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1d8e1-108">Remarks</span></span>

<span data-ttu-id="1d8e1-109">Wenn Sie ein clientseitiges [Recordset-Objekt](recordset-object-ado.md)verwenden, Datensätze, die auf dem Client geändert wurden zurückgeschrieben in der mittleren Ebene oder Webserver durch eine Technik Marshalling, das Packen und Senden der Parameter für die Benutzeroberfläche über Thread aufgerufen oder Grenzen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-109">When using a client-side [Recordset](recordset-object-ado.md), records that have been modified on the client are written back to the middle tier or web server through a technique called marshaling, the process of packaging and sending interface method parameters across thread or process boundaries.</span></span> <span data-ttu-id="1d8e1-110">Festlegen der **MarshalOptions** -Eigenschaft kann die Leistung verbessern, wenn geänderte Remotedaten zum Aktualisieren der wieder auf der mittleren Ebene oder Webserver gemarshallt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-110">Setting the **MarshalOptions** property can improve performance when modified remote data is marshaled for updating back to the middle tier or web server.</span></span>

<span data-ttu-id="1d8e1-111">**Remote Data Service-Verwendung** Diese Eigenschaft wird nur auf einem clientseitigen **Recordset-Objekt**verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d8e1-111">**Remote Data Service Usage**This property is used only on a client-side **Recordset**.</span></span>

