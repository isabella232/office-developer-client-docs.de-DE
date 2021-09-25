---
title: CommandText-Eigenschaft (ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: c2fd60d7e14b840a11d12069dbd72879167c3bae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565807"
---
# <a name="commandtext-property-ado"></a>CommandText-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Text eines Befehls an, der an einen Anbieter ausgegeben werden soll.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Mit dieser Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der einen Anbieterbefehl enthält, z. B. eine SQL-Anweisung, einen Tabellennamen, eine relative URL oder den Aufruf einer gespeicherten Prozedur. Die Standardeinstellung ist "" (leere Zeichenfolge).

## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **CommandText**-Eigenschaft, um den Text eines durch ein [Command](command-object-ado.md)-Objekt identifizierten Befehls festzulegen oder zurückzugeben. Gewöhnlich handelt es sich dabei um eine SQL-Anweisung. Möglich ist jedoch auch jede andere vom Anbieter erkannte Befehlsanweisung, wie z. B. ein Aufruf einer gespeicherten Prozedur. Eine SQL-Anweisung muss genau dem Dialekt oder der Version entsprechen, die vom Abfrageprozessor des Anbieters unterstützt werden.

Falls die [Prepared](prepared-property-ado.md)-Eigenschaft des **Command** -Objekts auf **True** festgelegt ist und das **Command** -Objekt an eine geöffnete Verbindung gebunden ist, wenn Sie die **CommandText** -Eigenschaft festlegen, bereitet ADO beim Aufrufen der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)- oder **Open** -Methode die Abfrage vor (d. h. eine kompilierte Form der vom Anbieter gespeicherten Abfrage).

In Abhängigkeit von der Einstellung für die [CommandType](commandtype-property-ado.md)-Eigenschaft wird die **CommandText** -Eigenschaft möglicherweise von ADO geändert. Sie können die **CommandText** -Eigenschaft jederzeit lesen, um den tatsächlichen Befehlstext anzuzeigen, den ADO bei der Ausführung verwenden wird.

Mit der **CommandText** -Eigenschaft können Sie eine relative URL festlegen oder zurückgeben, die eine Ressource angibt, wie z. B. eine Datei oder ein Verzeichnis. Die Ressource ist relativ zu einem explizit durch eine absolute URL angegebenen Speicherort oder implizit zu einem geöffneten [Connection](connection-object-ado.md)-Objekt.


> [!NOTE]
> Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs.](absolute-and-relative-urls.md)


