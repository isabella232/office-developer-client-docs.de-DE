---
title: ActualSize-Eigenschaft (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13cb41299ddaf786e6412e43a50b1414ad818b4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698204"
---
# <a name="actualsize-property-ado"></a><span data-ttu-id="28e9e-102">ActualSize-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="28e9e-102">ActualSize property (ADO)</span></span>

<span data-ttu-id="28e9e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28e9e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28e9e-104">Gibt die tatsächliche Länge des Werts eines Felds an.</span><span class="sxs-lookup"><span data-stu-id="28e9e-104">Indicates the actual length of a field's value.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="28e9e-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="28e9e-105">Settings and return values</span></span>

<span data-ttu-id="28e9e-p101">Gibt einen Wert vom Datentyp Long zurück. Für einige Anbieter kann diese Eigenschaft festgelegt werden, um Speicherplatz für BLOB-Daten zu reservieren. In diesem Fall lautet der Standardwert 0.</span><span class="sxs-lookup"><span data-stu-id="28e9e-p101">Returns a **Long** value. Some providers may allow this property to be set to reserve space for BLOB data, in which case the default value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="28e9e-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28e9e-108">Remarks</span></span>

<span data-ttu-id="28e9e-p102">Mithilfe der **ActualSize** -Eigenschaft geben Sie die tatsächliche Länge des Werts eines [Field](field-object-ado.md)-Objekts zurück. Die **ActualSize** -Eigenschaft ist für alle Felder schreibgeschützt. Falls ADO die Länge des Werts für das **Field** -Objekt nicht bestimmen kann, wird **adUnknown** von der **ActualSize** -Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="28e9e-p102">Use the **ActualSize** property to return the actual length of a [Field](field-object-ado.md) object's value. For all fields, the **ActualSize** property is read-only. If ADO cannot determine the length of the **Field** object's value, the **ActualSize** property returns **adUnknown**.</span></span>

<span data-ttu-id="28e9e-112">**ActualSize-** und [DefinedSize](definedsize-property-ado.md) -Eigenschaften sind unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="28e9e-112">The **ActualSize** and [DefinedSize](definedsize-property-ado.md) properties are different.</span></span> <span data-ttu-id="28e9e-113">Ein **Field** -Objekt mit dem deklarierten Typ **AdVarChar** und einer maximalen Länge von 50 Zeichen gibt zurück **DefinedSize** -Eigenschaft den Wert 50, aber des Werts der **ActualSize** -Eigenschaft gibt die Länge des Datenversion, die in das Feld für die Aktueller Datensatz.</span><span class="sxs-lookup"><span data-stu-id="28e9e-113">A **Field** object with a declared type of **adVarChar** and a maximum length of 50 characters returns a **DefinedSize** property value of 50, but the **ActualSize** property value it returns is the length of the data stored in the field for the current record.</span></span> <span data-ttu-id="28e9e-114">**Felder** mit einem **DefinedSize** größer als 255 Bytes als Spalten mit variabler Länge behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="28e9e-114">**Fields** with a **DefinedSize** greater than 255 bytes are treated as variable length columns.</span></span>

