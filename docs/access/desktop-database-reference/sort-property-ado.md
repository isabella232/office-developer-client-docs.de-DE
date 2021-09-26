---
title: Sort-Eigenschaft (ADO)
TOCTitle: Sort property (ADO)
ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15)
ms:contentKeyID: 48548652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ab12b9b32ac84cdd2b77959a1bdd23e4b868b4e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611497"
---
# <a name="sort-property-ado"></a>Sort-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt einen oder mehrere Feldnamen an, nach denen das [Recordset](recordset-object-ado.md) sortiert wird, und gibt an, ob die einzelnen Felder aufsteigend oder absteigend sortiert werden.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Legt einen **String**-Wert fest, der die Feldnamen im **Recordset**-Objekt angibt, nach denen sortiert wird, oder gibt den Wert zurück. Jeder Name wird durch ein Komma getrennt, ggf. gefolgt von einer Leerstelle und dem Schlüsselwort. **ASC** sortiert das Feld in aufsteigender, **DESC** in absteigender Reihenfolge. Wenn Sie kein Schlüsselwort angeben, wird das Feld standardmäßig in aufsteigender Reihenfolge sortiert.

## <a name="remarks"></a>HinwBemerkungeneise

Für diese Eigenschaft muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt sein. Ein temporärer Index wird für jedes Feld erstellt, das in der **Sort**-Eigenschaft angegeben ist, sofern noch kein Index vorhanden ist.

Der Sortiervorgang ist effizient, da Daten nicht physisch neu angeordnet werden, sondern einfach nur in der im Index angegebenen Reihenfolge auf die Daten zugegriffen wird.

Wenn Sie für die **Sort**-Eigenschaft eine leere Zeichenfolge festlegen, werden die Zeilen in die ursprüngliche Reihenfolge zurückgesetzt und temporäre Indizes gelöscht. Vorhandene Indizes werden nicht gelöscht.

Angenommen, ein **Recordset**-Objekt enthält drei Felder mit den Namen *firstName*, *middleInitial* und *lastName*. Legen Sie die **Sort-Eigenschaft** auf die Zeichenfolge "lastName DESC, firstName ASC" fest, die das **Recordset** nach dem Nachnamen in absteigender Reihenfolge und dann nach dem Vornamen in aufsteigender Reihenfolge sortiert. Der Mittelname wird ignoriert.

Felder können nicht "ASC" oder "DESC" benannt werden, da sonst ein Konflikt mit den Schlüsselwörtern **ASC** und **DESC** auftritt. Geben Sie einem Feld mit einem Konflikte verursachenden Namen einen Alias. Verwenden Sie dazu das Schlüsselwort **AS** in der Abfrage, die das **Recordset**-Objekt zurückgibt.

