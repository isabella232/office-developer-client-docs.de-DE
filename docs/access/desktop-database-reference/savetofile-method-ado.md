---
title: SaveToFile-Methode (ADO)
TOCTitle: SaveToFile Method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e1fcb4a5365f431eed4ed30ca57a3418abac9e2e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875462"
---
# <a name="savetofile-method-ado"></a><span data-ttu-id="66022-102">SaveToFile-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="66022-102">SaveToFile Method (ADO)</span></span>


<span data-ttu-id="66022-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66022-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="66022-104">Speichert den binären Inhalt eines [Stream](stream-object-ado.md)-Objekts in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="66022-104">Saves the binary contents of a [Stream](stream-object-ado.md) to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="66022-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="66022-105">Syntax</span></span>

<span data-ttu-id="66022-106">*Stream-Objekt*. SaveToFile*Dateiname*, *SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="66022-106">*Stream*.SaveToFile*FileName*, *SaveOptions*</span></span>

## <a name="parameters"></a><span data-ttu-id="66022-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="66022-107">Parameters</span></span>

  - <span data-ttu-id="66022-108">*FileName*</span><span class="sxs-lookup"><span data-stu-id="66022-108">*FileName*</span></span>

  - <span data-ttu-id="66022-p101">Ein **String** -Wert, der den vollqualifiziertern Namen der Datei enthält, in die der Inhalt des **Stream** -Objekts gespeichert wird. Sie können einen gültigen lokalen Speicherort oder einen Speicherort, auf den Sie über einen UNC-Wert zugreifen können, angeben.</span><span class="sxs-lookup"><span data-stu-id="66022-p101">A **String** value that contains the fully-qualified name of the file to which the contents of the **Stream** will be saved. You can save to any valid local location, or any location you have access to via a UNC value.</span></span>

  - <span data-ttu-id="66022-111">*SaveOptions*</span><span class="sxs-lookup"><span data-stu-id="66022-111">*SaveOptions*</span></span>

  - <span data-ttu-id="66022-p102">Ein [SaveOptionsEnum](saveoptionsenum.md)-Wert, der angibt, ob eine neue Datei mithilfe von **SaveToFile** erstellt werden soll, falls diese nicht bereits vorhanden ist. Der Standardwert lautet **adSaveCreateNotExists**. Mit diesen Optionen können Sie angeben, dass ein Fehler auftritt, falls die angegebene Datei nicht vorhanden ist. Sie können auch angeben, dass **SaveToFile** den aktuellen Inhalt einer vorhandenen Datei überschreibt.</span><span class="sxs-lookup"><span data-stu-id="66022-p102">A [SaveOptionsEnum](saveoptionsenum.md) value that specifies whether a new file should be created by **SaveToFile**, if it does not already exist. Default value is **adSaveCreateNotExists**. With these options you can specify that an error occurs if the specified file does not exist. You can also specify that **SaveToFile** overwrites the current contents of an existing file.</span></span>


> [!NOTE]
> <P><span data-ttu-id="66022-116">[!HINWEIS] Wenn Sie eine vorhandene Datei überschreiben (wenn <STRONG>adSaveCreateOverwrite</STRONG> festgelegt ist), ignoriert <STRONG>SaveToFile</STRONG> alle Bytes aus der vorhandenen ursprünglichen Datei, die dem neuen <A href="eos-property-ado.md">EOS</A> folgen.</span><span class="sxs-lookup"><span data-stu-id="66022-116">If you overwrite an existing file (when <STRONG>adSaveCreateOverwrite</STRONG> is set), <STRONG>SaveToFile</STRONG> truncates any bytes from the original existing file that follow the new <A href="eos-property-ado.md">EOS</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="66022-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66022-117">Remarks</span></span>

<span data-ttu-id="66022-p103">**SaveToFile** kann verwendet werden, um den Inhalt eines **Stream** -Objekts in eine lokale Datei zu speichern. Es werden keine Änderungen am Inhalt oder den Eigenschaften des **Stream** -Objekts vorgenommen. Das **Stream** -Objekt muss vor dem Aufrufen von **SaveToFile** geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="66022-p103">**SaveToFile** may be used to copy the contents of a **Stream** object to a local file. There is no change in the contents or properties of the **Stream** object. The **Stream** object must be open before calling **SaveToFile**.</span></span>

<span data-ttu-id="66022-p104">Diese Methode ändert die Zuordnung des **Stream** -Objekts zu dessen zugrunde liegender Quelle nicht. Das **Stream** -Objekt bleibt der ursprünglichen URL oder dem ursprünglichen **Record** -Objekt zugeordnet, die bzw. das beim Öffnen dessen Quelle darstellte.</span><span class="sxs-lookup"><span data-stu-id="66022-p104">This method does not change the association of the **Stream** object to its underlying source. The **Stream** object will still be associated with the original URL or **Record** that was its source when opened.</span></span>

<span data-ttu-id="66022-123">Nach einem **SaveToFile**-Vorgang wird die aktuelle Position ([Position](position-property-ado.md)) im Datenstrom auf den Anfang des Datenstroms festgelegt (0).</span><span class="sxs-lookup"><span data-stu-id="66022-123">After a **SaveToFile** operation, the current position ([Position](position-property-ado.md)) in the stream is set to the beginning of the stream (0).</span></span>

