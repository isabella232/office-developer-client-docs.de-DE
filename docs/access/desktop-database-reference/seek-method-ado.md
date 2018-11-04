---
title: Seek-Methode - ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be8127ea3f298a8f137012615b1f4de656a6ea1f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949712"
---
# <a name="seek-method-ado"></a><span data-ttu-id="dea56-102">Seek-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="dea56-102">Seek method (ADO)</span></span>

<span data-ttu-id="dea56-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dea56-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dea56-104">Durchsucht den Index eines [Recordset](recordset-object-ado.md)-Objekt, um auf schnelle Weise die Zeile zu finden, die den angegebenen Werten entspricht, und ändert die aktuelle Zeilenposition auf diese Zeile.</span><span class="sxs-lookup"><span data-stu-id="dea56-104">Searches the index of a [Recordset](recordset-object-ado.md) to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dea56-105">Syntax</span></span>

<span data-ttu-id="dea56-106">*Recordset-Objekt*. Seek*KeyValues entspricht*, *SeekOption*</span><span class="sxs-lookup"><span data-stu-id="dea56-106">*recordset*.Seek*KeyValues*, *SeekOption*</span></span>

## <a name="parameters"></a><span data-ttu-id="dea56-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dea56-107">Parameters</span></span>

|<span data-ttu-id="dea56-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dea56-108">Parameter</span></span>|<span data-ttu-id="dea56-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dea56-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="dea56-110">*KeyValues*</span><span class="sxs-lookup"><span data-stu-id="dea56-110">*KeyValues*</span></span> |<span data-ttu-id="dea56-p101">Ein Array mit **Variant** -Werten. Ein Index besteht aus einer oder mehreren Spalten, und das Array enthält einen Wert, mit dem jede einzelne Spalte verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="dea56-p101">An array of **Variant** values. An index consists of one or more columns and the array contains a value to compare against each corresponding column.</span></span>|
|<span data-ttu-id="dea56-113">*SeekOption*</span><span class="sxs-lookup"><span data-stu-id="dea56-113">*SeekOption*</span></span> |<span data-ttu-id="dea56-114">Ein [SeekEnum](seekenum.md)-Wert, der die Art des Vergleichs angibt, der zwischen den Spalten des Index und den entsprechenden *KeyValues* vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="dea56-114">A [SeekEnum](seekenum.md) value that specifies the type of comparison to be made between the columns of the index and the corresponding *KeyValues*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="dea56-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dea56-115">Remarks</span></span>

<span data-ttu-id="dea56-116">Verwenden Sie die **Seek** -Methode in Verbindung mit der [Index](index-property-ado.md)-Eigenschaft, falls der zugrunde liegende Anbieter Indizes für das **Recordset** -Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dea56-116">Use the **Seek** method in conjunction with the [Index](index-property-ado.md) property if the underlying provider supports indexes on the **Recordset** object.</span></span> <span data-ttu-id="dea56-117">Verwenden Sie die Methode, um zu bestimmen, ob der zugrunde liegenden Anbieter **Seek**unterstützt [unterstützt](supports-method-ado.md)**(AdSeek)** und die **Supports(adIndex)** -Methode, um festzustellen, ob der Anbieter Indizes unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dea56-117">Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes.</span></span> <span data-ttu-id="dea56-118">(Beispielsweise werden [Seek](microsoft-ole-db-provider-for-microsoft-jet.md) und **Index** vom **OLE DB-Anbieter für Microsoft Jet** unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="dea56-118">(For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="dea56-p103">Wenn **Seek** die gewünschte Zeile nicht findet, tritt kein Fehler auf, und die Zeile wird am Ende des **Recordset** -Objekts positioniert. Legen Sie die **Index** -Eigenschaft auf den gewünschten Index fest, bevor Sie diese Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="dea56-p103">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="dea56-p104">Diese Methode wird nur bei serverseitigen Cursors unterstützt. Seek wird nicht unterstützt, wenn der Wert der CursorLocation-Eigenschaft des Recordset-Objekts adUseClient lautet.</span><span class="sxs-lookup"><span data-stu-id="dea56-p104">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="dea56-123">Diese Methode kann nur verwendet werden, wenn das **Recordset** -Objekt mit einem [CommandTypeEnum](commandtypeenum.md)-Wert für **adCmdTableDirect** geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="dea56-123">This method can only be used when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

