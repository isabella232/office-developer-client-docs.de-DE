---
title: Feldbezogene Fehlerinformationen
TOCTitle: Field-Related Error Information
ms:assetid: 81a2c5a4-ab09-53d8-b270-e889b00a0c1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249559(v=office.15)
ms:contentKeyID: 48545958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de2a737e314322064894142b2494e3b3793d1625
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884856"
---
# <a name="field-related-error-information"></a><span data-ttu-id="a562d-102">Feldbezogene Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="a562d-102">Field-Related Error Information</span></span>


<span data-ttu-id="a562d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a562d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a562d-p101">Wenn sich ein Fehler direkt auf ein Feld bezieht - z. B., wenn die Daten fehlen oder wenn sie für das Feld den falschen Datentyp aufweisen - können Sie weitere Informationen zur Ursache des Problems abrufen, indem Sie die **Status** -Eigenschaft des **Field** -Objekts überprüfen. Diese Eigenschaft wurde optimiert und stellt nun spezifische Informationen zum Problem bereit. Wenn z. B. bei einem Aufruf von **UpdateBatch** ein Fehler erzeugt wird, kann die Ursache des Problems bestimmt werden, indem Sie die **Status** -Eigenschaft des **Fields** -Objekts in allen betroffenen Datensätzen überprüfen. Die Eigenschaft enthält einen der Werte in der **FieldStatusEnum** -Konstante. Die folgende Tabelle enthält die Werte, die beim Auftreten eines Fehlers von besonderem Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="a562d-p101">If an error is directly related to a field — for example, if the data is missing or if it is the wrong type for the field — you can retrieve more information about the cause of the problem by examining the **Field** object's **Status** property. This property has been enhanced to provide specific information about the problem. So, for example, when a call to **UpdateBatch** fails, the cause of the problem can be determined by examining the **Status** property of the **Fields** in each of the effected records. The property will contain one of the values in the **FieldStatusEnum** constant. The following table includes those values that are of particular interest when an error occurs.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a562d-109">Konstante</span><span class="sxs-lookup"><span data-stu-id="a562d-109">Constant</span></span></p></th>
<th><p><span data-ttu-id="a562d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a562d-110">Value</span></span></p></th>
<th><p><span data-ttu-id="a562d-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a562d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a562d-112"><strong>adFieldCantConvertValue</strong></span><span class="sxs-lookup"><span data-stu-id="a562d-112"><strong>adFieldCantConvertValue</strong></span></span></p></td>
<td><p><span data-ttu-id="a562d-113">2</span><span class="sxs-lookup"><span data-stu-id="a562d-113">2</span></span></p></td>
<td><p><span data-ttu-id="a562d-114">Gibt an, dass das Feld nicht ohne Datenverlust abgerufen oder gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="a562d-114">Indicates that the field cannot be retrieved or stored without loss of data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a562d-115"><strong>adFieldDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="a562d-115"><strong>adFieldDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="a562d-116">6</span><span class="sxs-lookup"><span data-stu-id="a562d-116">6</span></span></p></td>
<td><p><span data-ttu-id="a562d-117">Gibt an, dass die vom Anbieter zurückgegebenen Daten einen Überlauf beim Datentyp des Felds verursachten.</span><span class="sxs-lookup"><span data-stu-id="a562d-117">Indicates that the data returned from the provider overflowed the data type of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a562d-118"><strong>adFieldDefault</strong></span><span class="sxs-lookup"><span data-stu-id="a562d-118"><strong>adFieldDefault</strong></span></span></p></td>
<td><p><span data-ttu-id="a562d-119">13</span><span class="sxs-lookup"><span data-stu-id="a562d-119">13</span></span></p></td>
<td><p><span data-ttu-id="a562d-120">Gibt an, dass beim Festlegen von Daten der Standardwert verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="a562d-120">Indicates that the default value for the field was used when setting data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a562d-121"><strong>adFieldIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="a562d-121"><strong>adFieldIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="a562d-122">15</span><span class="sxs-lookup"><span data-stu-id="a562d-122">15</span></span></p></td>
<td><p><span data-ttu-id="a562d-p102">Gibt an, dass beim Festlegen von Datenwerten in der Quelle dieses Feld ausgelassen wurde. Vom Anbieter wurde kein Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a562d-p102">Indicates that this field was skipped when setting data values in the source. No value was set by the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a562d-125"><strong>adFieldIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="a562d-125"><strong>adFieldIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="a562d-126">10</span><span class="sxs-lookup"><span data-stu-id="a562d-126">10</span></span></p></td>
<td><p><span data-ttu-id="a562d-127">Gibt an, dass das Feld nicht geändert werden kann, da es eine berechnete oder abgeleitete Entität ist.</span><span class="sxs-lookup"><span data-stu-id="a562d-127">Indicates that the field cannot be modified because it is a calculated or derived entity.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a562d-128"><strong>adFieldIsNull</strong></span><span class="sxs-lookup"><span data-stu-id="a562d-128"><strong>adFieldIsNull</strong></span></span></p></td>
<td><p><span data-ttu-id="a562d-129">3</span><span class="sxs-lookup"><span data-stu-id="a562d-129">3</span></span></p></td>
<td><p><span data-ttu-id="a562d-130">Gibt an, dass der Anbieter einen NULL-Wert zurückgab.</span><span class="sxs-lookup"><span data-stu-id="a562d-130">Indicates that the provider returned a null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a562d-131"><strong>adFieldOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="a562d-131"><strong>adFieldOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="a562d-132">22</span><span class="sxs-lookup"><span data-stu-id="a562d-132">22</span></span></p></td>
<td><p><span data-ttu-id="a562d-133">Gibt an, dass der Anbieter nicht genügend Speicherplatz abrufen kann, um einen Verschiebe- oder Kopiervorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a562d-133">Indicates that the provider is unable to obtain enough storage space to complete a move or copy operation.</span></span></p></td>
</tr>
</tbody>
</table>

