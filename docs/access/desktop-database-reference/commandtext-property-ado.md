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
# <a name="commandtext-property-ado"></a><span data-ttu-id="467de-102">CommandText-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="467de-102">CommandText Property (ADO)</span></span>


<span data-ttu-id="467de-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="467de-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="467de-104">Gibt den Text eines Befehls an, der an einen Anbieter ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="467de-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="467de-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="467de-105">Settings and Return Values</span></span>

<span data-ttu-id="467de-p101">Mit dieser Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der einen Anbieterbefehl enthält, z. B. eine SQL-Anweisung, einen Tabellennamen, eine relative URL oder den Aufruf einer gespeicherten Prozedur. Die Standardeinstellung ist "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="467de-p101">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call. Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="467de-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="467de-108">Remarks</span></span>

<span data-ttu-id="467de-p102">Verwenden Sie die **CommandText** -Eigenschaft, um den Text eines durch ein [Command](command-object-ado.md)-Objekt identifizierten Befehls festzulegen oder zurückzugeben. Gewöhnlich handelt es sich dabei um eine SQL-Anweisung. Möglich ist jedoch auch jede andere vom Anbieter erkannte Befehlsanweisung, wie z. B. ein Aufruf einer gespeicherten Prozedur. Eine SQL-Anweisung muss genau dem Dialekt oder der Version entsprechen, die vom Abfrageprozessor des Anbieters unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="467de-p102">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object. Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call. An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="467de-112">Falls die [Prepared](prepared-property-ado.md)-Eigenschaft des **Command** -Objekts auf **True** festgelegt ist und das **Command** -Objekt an eine geöffnete Verbindung gebunden ist, wenn Sie die **CommandText** -Eigenschaft festlegen, bereitet ADO beim Aufrufen der [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))- oder **Open** -Methode die Abfrage vor (d. h. eine kompilierte Form der vom Anbieter gespeicherten Abfrage).</span><span class="sxs-lookup"><span data-stu-id="467de-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) or **Open** methods.</span></span>

<span data-ttu-id="467de-p103">In Abhängigkeit von der Einstellung für die [CommandType](commandtype-property-ado.md)-Eigenschaft wird die **CommandText** -Eigenschaft möglicherweise von ADO geändert. Sie können die **CommandText** -Eigenschaft jederzeit lesen, um den tatsächlichen Befehlstext anzuzeigen, den ADO bei der Ausführung verwenden wird.</span><span class="sxs-lookup"><span data-stu-id="467de-p103">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property. You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="467de-p104">Mit der **CommandText** -Eigenschaft können Sie eine relative URL festlegen oder zurückgeben, die eine Ressource angibt, wie z. B. eine Datei oder ein Verzeichnis. Die Ressource ist relativ zu einem explizit durch eine absolute URL angegebenen Speicherort oder implizit zu einem geöffneten [Connection](connection-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="467de-p104">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory. The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="467de-p105">[!HINWEIS] Für URLs, die das HTTP-Schema verwenden, wird automatisch der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB-Anbieter für Internet Publishing</A> aufgerufen. Weitere Informationen finden Sie unter <A href="absolute-and-relative-urls.md">Absolute und relative URLs</A>.</span><span class="sxs-lookup"><span data-stu-id="467de-p105">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


