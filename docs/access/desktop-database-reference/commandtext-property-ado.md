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
localization_priority: Normal
ms.openlocfilehash: 66797accb24cead7d7ba5732f0a9c58ee31049e5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725980"
---
# <a name="commandtext-property-ado"></a>CommandText-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt den Text eines Befehls an, der an einen Anbieter ausgegeben werden soll.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der einen Anbieterbefehl enthält, z. B. eine SQL-Anweisung, einen Tabellennamen, eine relative URL oder den Aufruf einer gespeicherten Prozedur. Die Standardeinstellung ist "" (leere Zeichenfolge).

## <a name="remarks"></a>Hinweise

Verwenden Sie die **CommandText** -Eigenschaft, um den Text eines durch ein [Command](command-object-ado.md)-Objekt identifizierten Befehls festzulegen oder zurückzugeben. Gewöhnlich handelt es sich dabei um eine SQL-Anweisung. Möglich ist jedoch auch jede andere vom Anbieter erkannte Befehlsanweisung, wie z. B. ein Aufruf einer gespeicherten Prozedur. Eine SQL-Anweisung muss genau dem Dialekt oder der Version entsprechen, die vom Abfrageprozessor des Anbieters unterstützt werden.

Falls die [Prepared](prepared-property-ado.md)-Eigenschaft des **Command** -Objekts auf **True** festgelegt ist und das **Command** -Objekt an eine geöffnete Verbindung gebunden ist, wenn Sie die **CommandText** -Eigenschaft festlegen, bereitet ADO beim Aufrufen der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)- oder **Open** -Methode die Abfrage vor (d. h. eine kompilierte Form der vom Anbieter gespeicherten Abfrage).

In Abhängigkeit von der Einstellung für die [CommandType](commandtype-property-ado.md)-Eigenschaft wird die **CommandText** -Eigenschaft möglicherweise von ADO geändert. Sie können die **CommandText** -Eigenschaft jederzeit lesen, um den tatsächlichen Befehlstext anzuzeigen, den ADO bei der Ausführung verwenden wird.

Mit der **CommandText** -Eigenschaft können Sie eine relative URL festlegen oder zurückgeben, die eine Ressource angibt, wie z. B. eine Datei oder ein Verzeichnis. Die Ressource ist relativ zu einem explizit durch eine absolute URL angegebenen Speicherort oder implizit zu einem geöffneten [Connection](connection-object-ado.md)-Objekt.


> [!NOTE]
> [!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).


