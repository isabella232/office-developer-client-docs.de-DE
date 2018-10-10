---
title: CommandText-Eigenschaft (ADO)
TOCTitle: CommandText Property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9000f069c7669872c686c013520f886d16e3619b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472695"
---
# <a name="commandtext-property-ado"></a>CommandText-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt den Text eines Befehls an, der an einen Anbieter ausgegeben werden soll.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der einen Anbieterbefehl enthält, z. B. eine SQL-Anweisung, einen Tabellennamen, eine relative URL oder den Aufruf einer gespeicherten Prozedur. Die Standardeinstellung ist "" (leere Zeichenfolge).

## <a name="remarks"></a>Hinweise

Verwenden Sie die **CommandText** -Eigenschaft, um den Text eines durch ein [Command](command-object-ado.md)-Objekt identifizierten Befehls festzulegen oder zurückzugeben. Gewöhnlich handelt es sich dabei um eine SQL-Anweisung. Möglich ist jedoch auch jede andere vom Anbieter erkannte Befehlsanweisung, wie z. B. ein Aufruf einer gespeicherten Prozedur. Eine SQL-Anweisung muss genau dem Dialekt oder der Version entsprechen, die vom Abfrageprozessor des Anbieters unterstützt werden.

Falls die [Prepared](prepared-property-ado.md)-Eigenschaft des **Command** -Objekts auf **True** festgelegt ist und das **Command** -Objekt an eine geöffnete Verbindung gebunden ist, wenn Sie die **CommandText** -Eigenschaft festlegen, bereitet ADO beim Aufrufen der [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))- oder **Open** -Methode die Abfrage vor (d. h. eine kompilierte Form der vom Anbieter gespeicherten Abfrage).

In Abhängigkeit von der Einstellung für die [CommandType](commandtype-property-ado.md)-Eigenschaft wird die **CommandText** -Eigenschaft möglicherweise von ADO geändert. Sie können die **CommandText** -Eigenschaft jederzeit lesen, um den tatsächlichen Befehlstext anzuzeigen, den ADO bei der Ausführung verwenden wird.

Mit der **CommandText** -Eigenschaft können Sie eine relative URL festlegen oder zurückgeben, die eine Ressource angibt, wie z. B. eine Datei oder ein Verzeichnis. Die Ressource ist relativ zu einem explizit durch eine absolute URL angegebenen Speicherort oder implizit zu einem geöffneten [Connection](connection-object-ado.md)-Objekt.


> [!NOTE]
> <P>[!HINWEIS] Für URLs, die das HTTP-Schema verwenden, wird automatisch der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB-Anbieter für Internet Publishing</A> aufgerufen. Weitere Informationen finden Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</P>


