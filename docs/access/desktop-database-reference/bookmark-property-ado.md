---
title: Bookmark-Eigenschaft (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 17818fe2b4f826cbcfbbb3955817c2b5d99ab6a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704770"
---
# <a name="bookmark-property-ado"></a>Bookmark-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt ein Lesezeichen an, das den aktuellen Datensatz in einem [Recordset](recordset-object-ado.md)-Objekt eindeutig identifiziert oder den aktuellen Datensatz in einem **Recordset** -Objekt auf den durch ein gültiges Lesezeichen identifizierten Datensatz festlegt.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Ausdruck vom Datentyp **Variant** festgelegt oder zurückgegeben, der in ein gültiges Lesezeichen ausgewertet wird.

## <a name="remarks"></a>Hinweise

Mithilfe der **Bookmark** -Eigenschaft speichern Sie die Position des aktuellen Datensatzes und können jederzeit zu diesem Datensatz zurückkehren. Lesezeichen sind nur in **Recordset** -Objekten verfügbar, die die Lesezeichenfunktionalität unterstützen.

Wenn Sie ein **Recordset** -Objekt öffnen, weist jeder Datensatz ein eindeutiges Lesezeichen auf. Weisen Sie der **Bookmark** -Eigenschaft eine Variable zu, um das Lesezeichen für den aktuellen Datensatz zu speichern. Um jederzeit schnell zu diesem Datensatz zurückkehren zu können, nachdem Sie zu einem anderen Datensatz navigiert sind, legen Sie die **Bookmark** -Eigenschaft des **Recordset** -Objekts auf den Wert dieser Variablen fest.

Möglicherweise kann der Benutzer den Wert des Lesezeichens nicht anzeigen. Außerdem sollten Benutzer nicht erwarten, dass Lesezeichen direkt vergleichbar sind; zwei Lesezeichen, die auf denselben Datensatz verweisen, können unterschiedliche Werte aufweisen.

Wenn Sie mithilfe der [Clone](clone-method-ado.md)-Methode eine Kopie eines **Recordset** -Objekts erstellen, sind die Einstellungen der **Bookmark** -Eigenschaft für das ursprüngliche und das duplizierte **Recordset** -Objekt identisch, und sie sind austauschbar. Lesezeichen von anderen **Recordset** -Objekten sind jedoch nicht austauschbar, selbst wenn sie von derselben Quelle oder von demselben Befehl erstellt wurden.

**Remote Data Service-Verwendung** Wenn für ein clientseitiges **Recordset** -Objekt verwendet wird, ist die **Bookmark** -Eigenschaft immer verfügbar.

