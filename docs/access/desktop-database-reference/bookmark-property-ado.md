---
title: Bookmark-Eigenschaft (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 17818fe2b4f826cbcfbbb3955817c2b5d99ab6a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704770"
---
# <a name="bookmark-property-ado"></a><span data-ttu-id="81e47-102">Bookmark-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="81e47-102">Bookmark property (ADO)</span></span>


<span data-ttu-id="81e47-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81e47-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81e47-104">Gibt ein Lesezeichen an, das den aktuellen Datensatz in einem [Recordset](recordset-object-ado.md)-Objekt eindeutig identifiziert oder den aktuellen Datensatz in einem **Recordset** -Objekt auf den durch ein gültiges Lesezeichen identifizierten Datensatz festlegt.</span><span class="sxs-lookup"><span data-stu-id="81e47-104">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="81e47-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="81e47-105">Settings and return values</span></span>

<span data-ttu-id="81e47-106">Mit dieser Eigenschaft wird ein Ausdruck vom Datentyp **Variant** festgelegt oder zurückgegeben, der in ein gültiges Lesezeichen ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="81e47-106">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="81e47-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81e47-107">Remarks</span></span>

<span data-ttu-id="81e47-p101">Mithilfe der **Bookmark** -Eigenschaft speichern Sie die Position des aktuellen Datensatzes und können jederzeit zu diesem Datensatz zurückkehren. Lesezeichen sind nur in **Recordset** -Objekten verfügbar, die die Lesezeichenfunktionalität unterstützen.</span><span class="sxs-lookup"><span data-stu-id="81e47-p101">Use the **Bookmark** property to save the position of the current record and return to that record at any time. Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="81e47-p102">Wenn Sie ein **Recordset** -Objekt öffnen, weist jeder Datensatz ein eindeutiges Lesezeichen auf. Weisen Sie der **Bookmark** -Eigenschaft eine Variable zu, um das Lesezeichen für den aktuellen Datensatz zu speichern. Um jederzeit schnell zu diesem Datensatz zurückkehren zu können, nachdem Sie zu einem anderen Datensatz navigiert sind, legen Sie die **Bookmark** -Eigenschaft des **Recordset** -Objekts auf den Wert dieser Variablen fest.</span><span class="sxs-lookup"><span data-stu-id="81e47-p102">When you open a **Recordset** object, each of its records has a unique bookmark. To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="81e47-p103">Möglicherweise kann der Benutzer den Wert des Lesezeichens nicht anzeigen. Außerdem sollten Benutzer nicht erwarten, dass Lesezeichen direkt vergleichbar sind; zwei Lesezeichen, die auf denselben Datensatz verweisen, können unterschiedliche Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="81e47-p103">The user may not be able to view the value of the bookmark. Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="81e47-p104">Wenn Sie mithilfe der [Clone](clone-method-ado.md)-Methode eine Kopie eines **Recordset** -Objekts erstellen, sind die Einstellungen der **Bookmark** -Eigenschaft für das ursprüngliche und das duplizierte **Recordset** -Objekt identisch, und sie sind austauschbar. Lesezeichen von anderen **Recordset** -Objekten sind jedoch nicht austauschbar, selbst wenn sie von derselben Quelle oder von demselben Befehl erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="81e47-p104">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably. However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="81e47-117">**Remote Data Service-Verwendung** Wenn für ein clientseitiges **Recordset** -Objekt verwendet wird, ist die **Bookmark** -Eigenschaft immer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="81e47-117">**Remote Data Service Usage**When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

