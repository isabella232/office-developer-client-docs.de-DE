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
ms.openlocfilehash: 86f69be8ed9216619f10bc70e2c701fb109d0ff5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879305"
---
# <a name="commandtext-property-ado"></a><span data-ttu-id="078de-102">CommandText-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="078de-102">CommandText property (ADO)</span></span>


<span data-ttu-id="078de-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="078de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="078de-104">Gibt den Text eines Befehls an, der an einen Anbieter ausgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="078de-104">Indicates the text of a command to be issued against a provider.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="078de-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="078de-105">Settings and return values</span></span>

<span data-ttu-id="078de-p101">Mit dieser Eigenschaft wird ein **String** -Wert festgelegt oder zurückgegeben, der einen Anbieterbefehl enthält, z. B. eine SQL-Anweisung, einen Tabellennamen, eine relative URL oder den Aufruf einer gespeicherten Prozedur. Die Standardeinstellung ist "" (leere Zeichenfolge).</span><span class="sxs-lookup"><span data-stu-id="078de-p101">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call. Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="078de-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="078de-108">Remarks</span></span>

<span data-ttu-id="078de-p102">Verwenden Sie die **CommandText** -Eigenschaft, um den Text eines durch ein [Command](command-object-ado.md)-Objekt identifizierten Befehls festzulegen oder zurückzugeben. Gewöhnlich handelt es sich dabei um eine SQL-Anweisung. Möglich ist jedoch auch jede andere vom Anbieter erkannte Befehlsanweisung, wie z. B. ein Aufruf einer gespeicherten Prozedur. Eine SQL-Anweisung muss genau dem Dialekt oder der Version entsprechen, die vom Abfrageprozessor des Anbieters unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="078de-p102">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object. Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call. An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="078de-112">Falls die [Prepared](prepared-property-ado.md)-Eigenschaft des **Command** -Objekts auf **True** festgelegt ist und das **Command** -Objekt an eine geöffnete Verbindung gebunden ist, wenn Sie die **CommandText** -Eigenschaft festlegen, bereitet ADO beim Aufrufen der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)- oder **Open** -Methode die Abfrage vor (d. h. eine kompilierte Form der vom Anbieter gespeicherten Abfrage).</span><span class="sxs-lookup"><span data-stu-id="078de-112">If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) or **Open** methods.</span></span>

<span data-ttu-id="078de-p103">In Abhängigkeit von der Einstellung für die [CommandType](commandtype-property-ado.md)-Eigenschaft wird die **CommandText** -Eigenschaft möglicherweise von ADO geändert. Sie können die **CommandText** -Eigenschaft jederzeit lesen, um den tatsächlichen Befehlstext anzuzeigen, den ADO bei der Ausführung verwenden wird.</span><span class="sxs-lookup"><span data-stu-id="078de-p103">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property. You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="078de-p104">Mit der **CommandText** -Eigenschaft können Sie eine relative URL festlegen oder zurückgeben, die eine Ressource angibt, wie z. B. eine Datei oder ein Verzeichnis. Die Ressource ist relativ zu einem explizit durch eine absolute URL angegebenen Speicherort oder implizit zu einem geöffneten [Connection](connection-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="078de-p104">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory. The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
> <span data-ttu-id="078de-117">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) automatisch aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="078de-117">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="078de-118">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="078de-118">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


