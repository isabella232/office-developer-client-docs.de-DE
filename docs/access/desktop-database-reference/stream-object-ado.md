---
title: Stream-Objekt (ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 75e0422b6c6fcd2f893777884d35bade81a793f6
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997042"
---
# <a name="stream-object-ado"></a><span data-ttu-id="92baa-102">Stream-Objekt (ADO)</span><span class="sxs-lookup"><span data-stu-id="92baa-102">Stream object (ADO)</span></span>


<span data-ttu-id="92baa-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92baa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92baa-104">Stellt einen Datenstrom von Binärdaten oder Text dar.</span><span class="sxs-lookup"><span data-stu-id="92baa-104">Represents a stream of binary data or text.</span></span>

## <a name="remarks"></a><span data-ttu-id="92baa-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="92baa-105">Remarks</span></span>

<span data-ttu-id="92baa-106">In strukturierten Hierarchien wie einem Dateisystem oder ein e-Mail-System möglicherweise einen [Datensatz](record-object-ado.md) einen binären Standarddatenstrom Bits zugeordnet, der den Inhalt der Datei oder die e-Mail enthält.</span><span class="sxs-lookup"><span data-stu-id="92baa-106">In tree-structured hierarchies such as a file system or an email system, a [Record](record-object-ado.md) may have a default binary stream of bits associated with it that contains the contents of the file or the email.</span></span> <span data-ttu-id="92baa-107">Mit einem **Stream** -Objekt können Felder oder Datensätze bearbeitet werden, die diese Datenströme enthalten.</span><span class="sxs-lookup"><span data-stu-id="92baa-107">A **Stream** object can be used to manipulate fields or records containing these streams of data.</span></span> <span data-ttu-id="92baa-108">Sie können ein **Stream** -Objekt auf folgende Weise erhalten:</span><span class="sxs-lookup"><span data-stu-id="92baa-108">A **Stream** object can be obtained in these ways:</span></span>

  - <span data-ttu-id="92baa-p102">Von einer URL, die auf ein Objekt (gewöhnlich eine Datei) zeigt, das die Binär- oder Textdaten enthält. Dieses Objekt kann ein einfaches Dokument, ein **Record** -Objekt, das ein strukturiertes Objekt darstellt, oder ein Ordner sein.</span><span class="sxs-lookup"><span data-stu-id="92baa-p102">From a URL pointing to an object (typically a file) containing binary or text data. This object can be a simple document, a **Record** object representing a structured document, or a folder.</span></span>

  - <span data-ttu-id="92baa-p103">Durch Öffnen des **Stream** -Objekts, das einem **Record** -Objekt zugeordnet ist. Sie erhalten den Standarddatenstrom, der einem **Record** -Objekt zugeordnet ist, wenn das **Record** -Objekt geöffnet wird, um einen Roundtrip zum Öffnen des Datenstroms zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="92baa-p103">By opening the default **Stream** object associated with a **Record** object. You can obtain the default stream associated with a **Record** object when the **Record** is opened, to eliminate a round-trip just to open the stream.</span></span>

  - <span data-ttu-id="92baa-p104">Durch Instanziieren eines **Stream** -Objekts. Dieses **Stream** -Objekt kann verwendet werden, um Daten für die Zwecke der Anwendung zu speichern. Im Unterschied zu einem **Stream** -Objekt, das einer URL zugeordnet ist, oder dem Standard- **Stream** -Objekt eines **Record** -Objekts ist ein instanziiertes **Stream** -Objekt keiner zugrunde liegenden Quelle standardmäßig zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="92baa-p104">By instantiating a **Stream** object. These **Stream** objects can be used to store data for the purposes of your application. Unlike a **Stream** associated with a URL, or the default **Stream** of a **Record**, an instantiated **Stream** has no association with an underlying source by default.</span></span>

<span data-ttu-id="92baa-116">Mit den Methoden und Eigenschaften eines **Stream** -Objekts können Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="92baa-116">With the methods and properties of a **Stream** object, you can do the following:</span></span>

  - <span data-ttu-id="92baa-117">Öffnen eines **Stream** -Objekts eines **Record** -Objekts oder URLs mit der [Open](open-method-ado-stream.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="92baa-117">Open a **Stream** object from a **Record** or URL with the [Open](open-method-ado-stream.md) method.</span></span>

  - <span data-ttu-id="92baa-118">Schließen eines **Stream** -Objekts mit der [Close](close-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="92baa-118">Close a **Stream** with the [Close](close-method-ado.md) method.</span></span>

  - <span data-ttu-id="92baa-119">Eingeben von Bytes oder Text in ein **Stream** -Objekt mit den Methoden [Write](write-method-ado.md) und [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="92baa-119">Input bytes or text to a **Stream** with the [Write](write-method-ado.md) and [WriteText](writetext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="92baa-120">Lesen von Bytes vom **Stream** -Objekt mit den Methoden [Read](read-method-ado.md) und [ReadText](readtext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="92baa-120">Read bytes from the **Stream** with the [Read](read-method-ado.md) and [ReadText](readtext-method-ado.md) methods.</span></span>

  - <span data-ttu-id="92baa-121">Schreiben beliebiger **Stream** -Daten, die noch im ADO-Puffer sind, in das zugrunde liegende Objekt mit der [Flush](flush-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="92baa-121">Write any **Stream** data still in the ADO buffer to the underlying object with the [Flush](flush-method-ado.md) method.</span></span>

  - <span data-ttu-id="92baa-122">Kopieren des Inhalts eines **Stream** -Objekts in ein anderes **Stream** -Objekt mit der [CopyTo](copyto-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="92baa-122">Copy the contents of a **Stream** to another **Stream** with the [CopyTo](copyto-method-ado.md) method.</span></span>

  - <span data-ttu-id="92baa-123">Steuern, wie Zeilen aus der Quelldatei gelesen werden, mit der [SkipLine](skipline-method-ado.md)-Methode und der [LineSeparator](lineseparator-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92baa-123">Control how lines are read from the source file with the [SkipLine](skipline-method-ado.md) method and the [LineSeparator](lineseparator-property-ado.md) property.</span></span>

  - <span data-ttu-id="92baa-124">Festlegen der Position des Datenstromendes mit der [EOS](eos-property-ado.md)-Eigenschaft und der [SetEOS](seteos-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="92baa-124">Determine the end of stream position with the [EOS](eos-property-ado.md) property and [SetEOS](seteos-method-ado.md) method.</span></span>

  - <span data-ttu-id="92baa-125">Speichern und Wiederherstellen von Daten in Dateien mit den Methoden [SaveToFile](savetofile-method-ado.md) und [LoadFromFile](loadfromfile-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="92baa-125">Save and restore data in files with the [SaveToFile](savetofile-method-ado.md) and [LoadFromFile](loadfromfile-method-ado.md) methods.</span></span>

  - <span data-ttu-id="92baa-126">Bestimmen des Zeichensatzes, der zum Speichern des **Stream** -Objekts verwendet wird, mit der [Charset](charset-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92baa-126">Specify the character set used for storing the **Stream** with the [Charset](charset-property-ado.md) property.</span></span>

  - <span data-ttu-id="92baa-127">Anhalten eines asynchronen **Stream** -Vorgangs mit der [Cancel](cancel-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="92baa-127">Halt an asynchronous **Stream** operation with the [Cancel](cancel-method-ado.md) method.</span></span>

  - <span data-ttu-id="92baa-128">Festlegen der Anzahl von Bytes in einem **Stream** -Objekt mit der [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92baa-128">Determine the number of bytes in a **Stream** with the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="92baa-129">Steuern der aktuellen Position innerhalb eines **Stream** -Objekts mit der [Position](position-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92baa-129">Control the current position within a **Stream** with the [Position](position-property-ado.md) property.</span></span>

  - <span data-ttu-id="92baa-130">Bestimmen des Typs der Daten in einem **Stream** -Objekt mit der [Type](type-property-ado-stream.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92baa-130">Determine the type of data in a **Stream** with the [Type](type-property-ado-stream.md) property.</span></span>

  - <span data-ttu-id="92baa-131">Bestimmen des aktuellen Zustands des **Stream** -Objekts (geschlossen, offen oder in Ausführung) mit der [State](state-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92baa-131">Determine the current state of the **Stream** (closed, open, or executing) with the [State](state-property-ado.md) property.</span></span>

  - <span data-ttu-id="92baa-132">Festlegen des Zugriffsmodus für das **Stream** -Objekt mit der [Mode](mode-property-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="92baa-132">Specify the access mode for the **Stream** with the [Mode](mode-property-ado.md) property.</span></span>

> [!NOTE]
> <span data-ttu-id="92baa-133">[!HINWEIS] Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="92baa-133">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="92baa-134">Weitere Informationen finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="92baa-134">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


