---
title: Parameters-Auflistung (ADO)
TOCTitle: Parameters collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 63af27d7856a737361def622e8547560aef8f1fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568740"
---
# <a name="parameters-collection-ado"></a>Parameters-Auflistung (ADO)


**Gilt für**: Access 2013, Office 2013

Enthält alle [Parameter](parameter-object-ado.md)-Objekte eines [Command](command-object-ado.md)-Objekts.

## <a name="remarks"></a>HinwBemerkungeneise

Ein **Command** -Objekt besitzt eine **Parameters** -Auflistung, die aus **Parameter** -Objekten besteht.

Mithilfe der [Refresh](refresh-method-ado.md)-Methode für eine **Parameters** -Auflistung eines **Command** -Objekts rufen Sie Anbieterparameterinformationen für die gespeicherte Prozedur oder parametrisierte Abfrage ab, die im **Command** -Objekt angegeben wist. Einige Anbieter unterstützen keine Aufrufe von gespeicherten Prozeduren oder parametrisierte Abfragen. Wenn Sie einen solchen Anbieter verwenden und die **Refresh** -Methode für die **Parameters** -Auflistung aufrufen, wird ein Fehler zurückgegeben.

Wenn Sie eigene **Parameter** -Objekte definiert haben und auf die **Parameters** -Auflistung zugreifen, bevor Sie die **Refresh** -Methode aufrufen, ruft ADO automatisch die Methode auf und füllt sie auf.

Sie können die Aufrufe des Providers zur Verbesserung der Leistung gering halten, wenn Sie die Eigenschaften der Parameter kennen, die der gespeicherten Prozedur oder der aufzurufenden parametrisierten Abfrage zugeordnet sind. Verwenden Sie die [CreateParameter](createparameter-method-ado.md)-Methode, um **Parameter** -Objekte mit den entsprechenden Eigenschaftseinstellungen zu erstellen, und verwenden Sie die [Append](append-method-ado.md)-Methode, um diese der **Parameters** -Auflistung hinzuzufügen. Auf diese Weise können Sie Parameterwerte festlegen und zurückgeben, ohne den Provider für die Parameterinformationen aufrufen zu müssen. Wenn Sie die Abfrage an einen Provider richten, der keine Parameterinformationen bereitstellt, müssen Sie die **Parameters** -Auflistung mit dieser Methode manuell zurückgeben, um Parameter verwenden zu können. Mit der [Delete](delete-method-ado-parameters-collection.md)-Methode können Sie **Parameter** -Objekte aus der **Parameters** -Auflistung entfernen, falls nötig.

Die Objekte in der **Parameters** -Auflistung eines **Recordset** -Objekts liegen außerhalb des Gültigkeitsbereichs (und sind somit nicht verfügbar), wenn das **Recordset** -Objekt geschlossen ist.

