---
title: Absolute und relative URLs
TOCTitle: Absolute and Relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc0cb3086f8fdfa032c005f7e2d219dab56999b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475406"
---
# <a name="absolute-and-relative-urls"></a><span data-ttu-id="b1e75-102">Absolute und relative URLs</span><span class="sxs-lookup"><span data-stu-id="b1e75-102">Absolute and Relative URLs</span></span>

<span data-ttu-id="b1e75-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1e75-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="b1e75-p101">Eine URL gibt den Speicherort eines auf einem lokalen oder vernetzten Computer gespeicherten Ziels an, z. B. eine Datei, ein Verzeichnis, eine HTML-Seite, ein Bild, ein Programm usw.\*\* In dieser Diskussion hat eine *absolute URL* dieses Format:</span><span class="sxs-lookup"><span data-stu-id="b1e75-p101">A URL specifies the location of a target stored on a local or networked computer, such as a file, directory, HTML page, image, program, and so on *.* In this discussion, an *absolute URL* is of the form:</span></span>

<span data-ttu-id="b1e75-106">*Schema://Server/Pfad/Ressource*</span><span class="sxs-lookup"><span data-stu-id="b1e75-106">*scheme://server/path/resource*</span></span>

<span data-ttu-id="b1e75-107">Dabei gilt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b1e75-107">where:</span></span>

  - <span data-ttu-id="b1e75-108">*Schema*</span><span class="sxs-lookup"><span data-stu-id="b1e75-108">*scheme*</span></span>

  - <span data-ttu-id="b1e75-109">Gibt an, wie die *Ressource* zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="b1e75-109">Specifies how the *resource* is to be accessed.</span></span>

  - <span data-ttu-id="b1e75-110">*Server*</span><span class="sxs-lookup"><span data-stu-id="b1e75-110">*server*</span></span>

  - <span data-ttu-id="b1e75-111">Gibt den Namen des Computers, auf dem die *Ressource* befindet.</span><span class="sxs-lookup"><span data-stu-id="b1e75-111">Specifies the name of the computer where the *resource* is located.</span></span>

  - <span data-ttu-id="b1e75-112">*Pfad*</span><span class="sxs-lookup"><span data-stu-id="b1e75-112">*path*</span></span>

  - <span data-ttu-id="b1e75-p102">Die Sequenz der zum Ziel führenden Verzeichnisse wird angegeben. Wenn *Ressource* weggelassen wird, ist das Ziel das letzte Verzeichnis im *Pfad*.</span><span class="sxs-lookup"><span data-stu-id="b1e75-p102">Specifies the sequence of directories leading to the target. If *resource* is omitted, the target is the last directory in *path*.</span></span>

  - <span data-ttu-id="b1e75-115">*Ressource*</span><span class="sxs-lookup"><span data-stu-id="b1e75-115">*resource*</span></span>

  - <span data-ttu-id="b1e75-116">Wenn enthalten, *Ressource* ist das Ziel und ist in der Regel der Name einer Datei.</span><span class="sxs-lookup"><span data-stu-id="b1e75-116">If included, *resource* is the target, and is typically the name of a file.</span></span> <span data-ttu-id="b1e75-117">Es kann eine *einfache Datei* , die einen einzelnen binären Stream von Bytes oder ein *strukturiertes Dokument* , enthält einen Speicher und binären enthält sein.</span><span class="sxs-lookup"><span data-stu-id="b1e75-117">It may be a *simple file,* containing a single binary stream of bytes, or a *structured document,* containing one or more storages and binary streams of bytes.</span></span>

<span data-ttu-id="b1e75-118">Eine *absolute URL* enthält alle Informationen zum Suchen einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="b1e75-118">An *absolute URL* contains all the information necessary to locate a resource.</span></span>

<span data-ttu-id="b1e75-p104">Durch eine *relative URL* wird eine Ressource mithilfe einer absoluten URL als Ausgangspunkt gesucht. Tatsächlich wird die "vollständige URL" des Ziels durch Verketten der absoluten und relativen URLs angegeben. Eine relative URL besteht normalerweise nur aus dem *Pfad* und optional aus der *Ressource*, enthält jedoch kein *Schema* und keinen *Server*.</span><span class="sxs-lookup"><span data-stu-id="b1e75-p104">A *relative URL* locates a resource using an absolute URL as a starting point. In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs. A relative URL typically consists only of the *path*, and optionally, the *resource*, but no *scheme* or *server*.</span></span>

## <a name="url-scheme-registration"></a><span data-ttu-id="b1e75-122">URL-Schemaregistrierung</span><span class="sxs-lookup"><span data-stu-id="b1e75-122">URL Scheme Registration</span></span>

<span data-ttu-id="b1e75-123">Wenn von einem Anbieter URLs unterstützt werden, wird mindestens ein URL-Schema für den Anbieter registriert.</span><span class="sxs-lookup"><span data-stu-id="b1e75-123">If a provider supports URLs, it will register for one or more URL schemes.</span></span> <span data-ttu-id="b1e75-124">Das heißt, dass durch alle URLs, in denen dieses Schema verwendet wird, automatisch der registrierte Anbieter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b1e75-124">This means that any URLs using this scheme will automatically invoke the registered provider.</span></span> <span data-ttu-id="b1e75-125">Beispielsweise ist das *http-* Schema für den [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)registriert.</span><span class="sxs-lookup"><span data-stu-id="b1e75-125">For example, the *http* scheme is registered to the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="b1e75-126">In ADO wird davon ausgegangen, dass alle URLs mit dem Präfix "http" Webordner oder mit dem Internet Publishing-Anbieter zu verwendende Dateien darstellen.</span><span class="sxs-lookup"><span data-stu-id="b1e75-126">ADO assumes all URLs prefixed with "http" represent Web folders or files to be used with the Internet Publishing Provider.</span></span> <span data-ttu-id="b1e75-127">Weitere Informationen zu den für den Anbieter registrierten Schemas finden Sie in der Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="b1e75-127">For information about the schemes registered by your provider, see your provider documentation.</span></span>

## <a name="defining-context-with-a-url"></a><span data-ttu-id="b1e75-128">Definieren von Kontext mit einer URL</span><span class="sxs-lookup"><span data-stu-id="b1e75-128">Defining Context with a URL</span></span>

<span data-ttu-id="b1e75-p106">Eine Funktion einer geöffneten Verbindung, die durch ein [Connection](connection-object-ado.md)-Objekt dargestellt wird, ist die Einschränkung nachfolgender Operationen auf die durch diese Verbindung dargestellte Datenquelle. Das heißt, der Kontext für nachfolgende Operationen wird durch die Verbindung definiert.</span><span class="sxs-lookup"><span data-stu-id="b1e75-p106">One function of an open connection, represented by a [Connection](connection-object-ado.md) object, is to restrict subsequent operations to the data source represented by that connection. That is, the connection defines the context for subsequent operations.</span></span>

<span data-ttu-id="b1e75-p107">Mit ADO 2.5 kann ein Kontext auch durch eine absolute URL definiert werden. Wenn z. B. ein [Record](record-object-ado.md)-Objekt mit einer absoluten URL geöffnet wird, wird implizit ein **Connection** -Objekt erstellt, das die durch die URL angegebene Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1e75-p107">With ADO 2.5, an absolute URL may also define a context. For example, when a [Record](record-object-ado.md) object is opened with an absolute URL, a **Connection** object is implicitly created to represent the resource specified by the URL.</span></span>

<span data-ttu-id="b1e75-133">Eine absolute URL, die definiert einen Kontext kann in der *ActiveConnection* -Parameter der [Open](open-method-ado-record.md) -Methode des **Record** -Objekts angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b1e75-133">An absolute URL that defines a context may be specified in the *ActiveConnection* parameter of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="b1e75-134">Eine absolute URL kann auch angegeben werden, als der Wert der neuen "URL**=**"-Schlüsselwort in der **Connection** -Objekt-Parameter *ConnectionString* [Open](open-method-ado-connection.md) -Methode und der [Open](open-method-ado-recordset.md) -Methode \*ActiveConnection für das [Recordset](recordset-object-ado.md) -Objekt \*Parameter.</span><span class="sxs-lookup"><span data-stu-id="b1e75-134">An absolute URL may also be specified as the value of the new "URL**=**" keyword in the **Connection** object [Open](open-method-ado-connection.md) method *ConnectionString* parameter, and the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method *ActiveConnection* parameter.</span></span>

<span data-ttu-id="b1e75-135">Der Kontext kann auch durch ein geöffnetes **Record** - oder **Recordset** -Objekt, das ein Verzeichnis darstellt, definiert werden, da diese Objekte bereits über ein implizit oder explizit deklariertes **Connection** -Objekt verfügen, durch das der Kontext angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1e75-135">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span></span>

## <a name="scoped-operations"></a><span data-ttu-id="b1e75-136">Bereichsvorgänge</span><span class="sxs-lookup"><span data-stu-id="b1e75-136">Scoped Operations</span></span>

<span data-ttu-id="b1e75-137">Der Kontext definiert einen *Bereich* gleichzeitig – d. h., des Verzeichnisses und seiner Unterverzeichnisse, die in den folgenden Vorgängen beteiligt sein können.</span><span class="sxs-lookup"><span data-stu-id="b1e75-137">The context simultaneously defines a *scope* — that is, the directory and its subdirectories that may participate in subsequent operations.</span></span> <span data-ttu-id="b1e75-138">Das **Record** -Objekt verfügt über mehrere bereichsbezogenen Methoden, einschließlich [CopyRecord](copyrecord-method-ado.md), [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), und [MoveRecord](moverecord-method-ado.md), die auf ein Verzeichnis und alle Unterverzeichnisse ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b1e75-138">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), that operate on a directory and all its subdirectories.</span></span>

## <a name="relative-urls-as-command-text"></a><span data-ttu-id="b1e75-139">Relative URLs als Befehlstext</span><span class="sxs-lookup"><span data-stu-id="b1e75-139">Relative URLs as Command Text</span></span>

<span data-ttu-id="b1e75-140">In der **Connection** -Objekt **Execute** -Methode *CommandText* -Parameter und der **Recordset** -Objekt **Open** -Methode *Source* -Parameter kann eine Zeichenfolge zur Angabe eines für die Datenquelle auszuführender Befehls angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b1e75-140">A string specifying a command to be executed on the data source may be specified in the **Connection** object **Execute** method *CommandText* parameter, and the **Recordset** object **Open** method *Source* parameter.</span></span>

<span data-ttu-id="b1e75-141">Eine relative URL kann im *CommandText* oder *Source* -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b1e75-141">A relative URL may be specified in the *CommandText* or *Source* parameter.</span></span> <span data-ttu-id="b1e75-142">Die relative URL gibt keine tatsächlich einen Befehl (beispielsweise einen SQL-Befehl); Es wird lediglich in diesen Parametern angegeben.</span><span class="sxs-lookup"><span data-stu-id="b1e75-142">The relative URL does not actually specify a command (such as an SQL command); it is merely specified in those parameters.</span></span> <span data-ttu-id="b1e75-143">Darüber hinaus muss im Kontext der aktiven Verbindung eine absolute URL sein, und der *Option* -Parameter muss auf **AdCmdTableDirect**festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="b1e75-143">In addition, the context of the active connection must be an absolute URL, and the *Option* parameter must be set to **adCmdTableDirect**.</span></span>

<span data-ttu-id="b1e75-144">Beispielsweise kann ein Recordset-Objekt wie folgt für die Datei Readme25.txt im Verzeichnis Winnt/system32 geöffnet werden:</span><span class="sxs-lookup"><span data-stu-id="b1e75-144">For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:</span></span>

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<span data-ttu-id="b1e75-145">Die absolute URL in der Verbindungszeichenfolge gibt den Server (YourServer) und der Pfad () und den Pfad (Winnt).</span><span class="sxs-lookup"><span data-stu-id="b1e75-145">The absolute URL in the connection string specifies the server (YourServer ) and the path () and the path (Winnt ).</span></span> <span data-ttu-id="b1e75-146">Durch diese URL wird auch der Kontext definiert.</span><span class="sxs-lookup"><span data-stu-id="b1e75-146">This URL also defines the context.</span></span>

<span data-ttu-id="b1e75-147">Die relative URL im Befehlstext wird die absolute URL als Ausgangspunkt und der restliche Pfad (system32) und die Datei zu öffnen () und die Datei (Readme25.txt) geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b1e75-147">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (system32 ) and the file to open () and the file to open (Readme25.txt ).</span></span>

<span data-ttu-id="b1e75-148">Das Feld (Optionen) gibt an, dass der Befehlstyp eine relative URL ist.</span><span class="sxs-lookup"><span data-stu-id="b1e75-148">The options field () indicates that the command type is a relative URL.</span></span>

<span data-ttu-id="b1e75-149">Als weiteres Beispiel wird mit dem folgende Code ein **Recordset-Objekt** auf den Inhalt des Verzeichnisses geöffnet:</span><span class="sxs-lookup"><span data-stu-id="b1e75-149">As another example, the following code will open a **Recordset** on the contents of the directory:</span></span>

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a><span data-ttu-id="b1e75-150">Vom OLE DB-Anbieter bereitgestellte URL-Schemas</span><span class="sxs-lookup"><span data-stu-id="b1e75-150">OLE DB Provider-Supplied URL Schemes</span></span>

<span data-ttu-id="b1e75-151">Vorderer Teil der eine voll qualifizierte URL wird das *Schema* verwendet, um die durch den Rest der URL angegebene Ressource zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b1e75-151">The leading part of a fully-qualified URL is the *scheme* used to access the resource identified by the remainder of the URL.</span></span> <span data-ttu-id="b1e75-152">Beispiele sind HTTP (HyperText Transfer Protocol) und FTP (File Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="b1e75-152">Examples are HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).</span></span>

<span data-ttu-id="b1e75-p113">In ADO werden OLE DB-Anbieter unterstützt, von denen die eigenen URL-Schemas erkannt werden. Beispielsweise wird vom [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* durch den auf "veröffentlichte" Windows 2000-Dateien zugegriffen wird, das vorhandene HTTP-Schema erkannt.</span><span class="sxs-lookup"><span data-stu-id="b1e75-p113">ADO supports OLE DB providers that recognize their own URL schemes. For example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</span></span>

