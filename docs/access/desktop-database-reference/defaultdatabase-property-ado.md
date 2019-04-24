---
title: DefaultDatabase-Eigenschaft (ADO)
TOCTitle: DefaultDatabase property (ADO)
ms:assetid: a35c5631-f9d9-e51f-950b-e52169830d94
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249757(v=office.15)
ms:contentKeyID: 48546784
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 01ca42ff738afe3a35cab6263cdae32ac256f3d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294148"
---
# <a name="defaultdatabase-property-ado"></a><span data-ttu-id="8658d-102">DefaultDatabase-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="8658d-102">DefaultDatabase property (ADO)</span></span>


<span data-ttu-id="8658d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8658d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8658d-104">Gibt die Standarddatenbank für ein [Connection](connection-object-ado.md)-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8658d-104">Indicates the default database for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8658d-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8658d-105">Settings and return values</span></span>

<span data-ttu-id="8658d-106">Mit dieser Eigenschaft wird ein **String**-Wert festgelegt oder zurückgegeben, der den Namen einer Datenbank angibt, die über den Anbieter verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="8658d-106">Sets or returns a **String** value that evaluates to the name of a database available from the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="8658d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8658d-107">Remarks</span></span>

<span data-ttu-id="8658d-108">Verwenden Sie die **DefaultDatabase**-Eigenschaft, um den Namen der Standarddatenbank in einem bestimmten **Connection**-Objekt festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8658d-108">Use the **DefaultDatabase** property to set or return the name of the default database on a specific **Connection** object.</span></span>

<span data-ttu-id="8658d-p101">Wenn eine Standarddatenbank vorhanden ist, verwenden SQL-Zeichenfolgen möglicherweise eine unvollständige Syntax für den Zugriff auf Objekte in dieser Datenbank. Für den Zugriff auf Objekte in einer anderen als der in der **DefaultDatabase**-Eigenschaft angegebenen Datenbank müssen Sie Objektnamen mit dem gewünschten Datenbanknamen qualifizieren. Beim Herstellen der Verbindung schreibt der Anbieter Informationen zur Standarddatenbank in die **DefaultDatabase**-Eigenschaft. Manche Anbieter lassen nur eine Datenbank pro Verbindung zu. In diesem Fall können Sie die **DefaultDatabase**-Eigenschaft nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="8658d-p101">If there is a default database, SQL strings may use an unqualified syntax to access objects in that database. To access objects in a database other than the one specified in the **DefaultDatabase** property, you must qualify object names with the desired database name. Upon connection, the provider will write default database information to the **DefaultDatabase** property. Some providers allow only one database per connection, in which case you cannot change the **DefaultDatabase** property.</span></span>

<span data-ttu-id="8658d-113">Möglicherweise unterstützen einige Datenquellen und Anbieter dieses Feature nicht und geben einen Fehler oder eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="8658d-113">Some data sources and providers may not support this feature, and may return an error or an empty string.</span></span>

<span data-ttu-id="8658d-114">**Remote Data Service-Verwendung** Diese Eigenschaft ist für ein clientseitiges **Connection** -Objekt nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8658d-114">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

