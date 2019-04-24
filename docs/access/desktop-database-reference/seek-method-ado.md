---
title: Seek-Methode – ActiveX Data Objects (ADO)
TOCTitle: Seek method (ADO)
ms:assetid: cf0f133b-31f2-a2df-6cf3-1b5fa73b516c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250027(v=office.15)
ms:contentKeyID: 48547802
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 321040a39b02f31f0265df6e91748df13c05032c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308792"
---
# <a name="seek-method-ado"></a><span data-ttu-id="001b6-102">Seek-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="001b6-102">Seek method (ADO)</span></span>

<span data-ttu-id="001b6-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="001b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="001b6-104">Durchsucht den Index eines [Recordset](recordset-object-ado.md)-Objekt, um auf schnelle Weise die Zeile zu finden, die den angegebenen Werten entspricht, und ändert die aktuelle Zeilenposition auf diese Zeile.</span><span class="sxs-lookup"><span data-stu-id="001b6-104">Searches the index of a [Recordset](recordset-object-ado.md) to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span>

## <a name="syntax"></a><span data-ttu-id="001b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="001b6-105">Syntax</span></span>

<span data-ttu-id="001b6-106">*Recordset*. Seek\*\*-keyValues, *SeekOption*</span><span class="sxs-lookup"><span data-stu-id="001b6-106">*recordset*.Seek*KeyValues*, *SeekOption*</span></span>

## <a name="parameters"></a><span data-ttu-id="001b6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="001b6-107">Parameters</span></span>

|<span data-ttu-id="001b6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="001b6-108">Parameter</span></span>|<span data-ttu-id="001b6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="001b6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="001b6-110">*KeyValues*</span><span class="sxs-lookup"><span data-stu-id="001b6-110">*KeyValues*</span></span> |<span data-ttu-id="001b6-p101">Ein Array mit **Variant** -Werten. Ein Index besteht aus einer oder mehreren Spalten, und das Array enthält einen Wert, mit dem jede einzelne Spalte verglichen wird.</span><span class="sxs-lookup"><span data-stu-id="001b6-p101">An array of **Variant** values. An index consists of one or more columns and the array contains a value to compare against each corresponding column.</span></span>|
|<span data-ttu-id="001b6-113">*SeekOption*</span><span class="sxs-lookup"><span data-stu-id="001b6-113">*SeekOption*</span></span> |<span data-ttu-id="001b6-114">Ein [SeekEnum](seekenum.md)-Wert, der die Art des Vergleichs angibt, der zwischen den Spalten des Index und den entsprechenden *KeyValues* vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="001b6-114">A [SeekEnum](seekenum.md) value that specifies the type of comparison to be made between the columns of the index and the corresponding *KeyValues*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="001b6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="001b6-115">Remarks</span></span>

<span data-ttu-id="001b6-p102">Verwenden Sie die **Seek**-Methode in Verbindung mit der [Index](index-property-ado.md)-Eigenschaft, falls der zugrunde liegende Anbieter Indizes für das **Recordset**-Objekt unterstützt. Mit der [Supports](supports-method-ado.md)**(adSeek)**-Methode bestimmen Sie, ob der zugrunde liegende Anbieter **Seek** unterstützt, und mit der **Supports(adIndex)**-Methode, ob der Anbieter Indizes unterstützt. (Beispielsweise werden **Seek** und **Index** vom [OLE DB-Anbieter für Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) unterstützt.)</span><span class="sxs-lookup"><span data-stu-id="001b6-p102">Use the **Seek** method in conjunction with the [Index](index-property-ado.md) property if the underlying provider supports indexes on the **Recordset** object. Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes. (For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="001b6-p103">Wenn **Seek** die gewünschte Zeile nicht findet, tritt kein Fehler auf, und die Zeile wird am Ende des **Recordset** -Objekts positioniert. Legen Sie die **Index** -Eigenschaft auf den gewünschten Index fest, bevor Sie diese Methode ausführen.</span><span class="sxs-lookup"><span data-stu-id="001b6-p103">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="001b6-p104">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="001b6-p104">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="001b6-123">Diese Methode kann nur verwendet werden, wenn das **Recordset** -Objekt mit einem [CommandTypeEnum](commandtypeenum.md)-Wert für **adCmdTableDirect** geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="001b6-123">This method can only be used when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

