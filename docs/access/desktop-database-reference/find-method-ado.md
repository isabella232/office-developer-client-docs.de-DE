---
title: Find-Methode - ActiveX Data Objects (ADO)
TOCTitle: Find Method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929e4ac695ff65c3576f2ffb8ad1baf8ab1d1137
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870625"
---
# <a name="find-method-ado"></a><span data-ttu-id="a0b7a-102">Find-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-102">Find Method (ADO)</span></span>


<span data-ttu-id="a0b7a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0b7a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a0b7a-p101">Durchsucht ein [Recordset](recordset-object-ado.md)-Objekt nach der Zeile, die den angegebenen Kriterien entspricht. Optional können die Suchrichtung, die Startzeile und der Versatz von der Startzeile aus gesehen angegeben werden. Stimmen die Kriterien überein, wird die aktuelle Zeilenposition bei dem gefundenen Datensatz festgelegt. Andernfalls wird die Startposition auf das Ende (oder den Anfang) des **Recordset** -Objekts festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-p101">Searches a [Recordset](recordset-object-ado.md) for the row that satisfies the specified criteria. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criteria is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b7a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0b7a-107">Syntax</span></span>

<span data-ttu-id="a0b7a-108">Hier finden Sie (*Kriterien*, *SkipRows*, *SearchDirection*, *Starten*)</span><span class="sxs-lookup"><span data-stu-id="a0b7a-108">Find (*Criteria*, *SkipRows*, *SearchDirection*, *Start*)</span></span>

## <a name="parameters"></a><span data-ttu-id="a0b7a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0b7a-109">Parameters</span></span>

  - <span data-ttu-id="a0b7a-110">*Criteria*</span><span class="sxs-lookup"><span data-stu-id="a0b7a-110">*Criteria*</span></span>

  - <span data-ttu-id="a0b7a-111">Ein **String** -Wert mit einer Anweisung, die den Spaltennamen, den Vergleichsoperator und den für die Suche zu verwendenden Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-111">A **String** value that contains a statement specifying the column name, comparison operator, and value to use in the search.</span></span>

  - <span data-ttu-id="a0b7a-112">*SkipRows*</span><span class="sxs-lookup"><span data-stu-id="a0b7a-112">*SkipRows*</span></span>

  - <span data-ttu-id="a0b7a-113">Optionale *.*</span><span class="sxs-lookup"><span data-stu-id="a0b7a-113">Optional *.*</span></span> <span data-ttu-id="a0b7a-114">Ein **Long** -Wert, dessen Standardwert 0 (null) ist,, der angibt, den Zeilenoffset aus der aktuellen Zeile oder die Textmarke *Starten ist* , um die Suche zu starten.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-114">A **Long** value, whose default value is zero, that specifies the row offset from the current row or *Start* bookmark to begin the search.</span></span> <span data-ttu-id="a0b7a-115">Standardmäßig beginnt die Suche bei der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-115">By default, the search will start on the current row.</span></span>

  - <span data-ttu-id="a0b7a-116">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="a0b7a-116">*SearchDirection*</span></span>

  - <span data-ttu-id="a0b7a-117">Optionale *.*</span><span class="sxs-lookup"><span data-stu-id="a0b7a-117">Optional *.*</span></span> <span data-ttu-id="a0b7a-118">Ein [SearchDirectionEnum](searchdirectionenum.md) -Wert, der angibt, ob die Suche auf der aktuellen Zeile oder die nächste verfügbare Zeile in der Richtung der Suche beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-118">A [SearchDirectionEnum](searchdirectionenum.md) value that specifies whether the search should begin on the current row or the next available row in the direction of the search.</span></span> <span data-ttu-id="a0b7a-119">Eine Suche nicht erfolgreiche beendet am Ende des **Recordset-Objekt** , wenn der Wert **AdSearchForward**ist.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-119">An unsuccessful search stops at the end of the **Recordset** if the value is **adSearchForward**.</span></span> <span data-ttu-id="a0b7a-120">Eine Suche nicht erfolgreiche beendet am Anfang des **Recordset-Objekt** , wenn der Wert **AdSearchBackward**ist.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-120">An unsuccessful search stops at the start of the **Recordset** if the value is **adSearchBackward**.</span></span>

  - <span data-ttu-id="a0b7a-121">*Start*</span><span class="sxs-lookup"><span data-stu-id="a0b7a-121">*Start*</span></span>

  - <span data-ttu-id="a0b7a-p104">Optional. Eine **Variant** -Textmarke, die als Startposition für die Suche fungiert.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-p104">Optional. A **Variant** bookmark that functions as the starting position for the search.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b7a-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a0b7a-124">Remarks</span></span>

<span data-ttu-id="a0b7a-p105">Es kann nur ein einzelner Spaltennamen für *Criteria* angegeben werden. Diese Methode unterstützt keine Suchen über mehrere Spalten.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-p105">Only a single-column name may be specified in *criteria*. This method does not support multi-column searches.</span></span>

<span data-ttu-id="a0b7a-127">Der Vergleichsoperator in *Kriterien* möglicherweise "**\>**"(größer als),"**\<**"(kleiner als), "=" (gleich),"\>=" (größer als oder gleich), "\<=" (kleiner als oder gleich), "\<\>" (nicht gleich) oder "like" (Mustervergleich).</span><span class="sxs-lookup"><span data-stu-id="a0b7a-127">The comparison operator in *Criteria* may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "like" (pattern matching).</span></span>

<span data-ttu-id="a0b7a-128">Der Wert in *Kriterien* möglicherweise eine Zeichenfolge, eine Gleitkommazahl oder ein Datum.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-128">The value in *Criteria* may be a string, floating-point number, or date.</span></span> <span data-ttu-id="a0b7a-129">String-Werte werden in einfache Anführungszeichen getrennt oder "\#" (Nummernzeichen) markiert (beispielsweise "State = 'WA'" oder "Zustand = \#WA\#").</span><span class="sxs-lookup"><span data-stu-id="a0b7a-129">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="a0b7a-130">Datumswerte sind mit getrennt "\#" (Nummernzeichen) markiert (beispielsweise "starten\_Datum \> \#7/22/97\#") und kann enthalten Stunden, Minuten und Sekunden an, dass Zeitstempel aber darf keine Millisekunden oder kommt es zu Fehlern .</span><span class="sxs-lookup"><span data-stu-id="a0b7a-130">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#") and can contain hours, minutes and seconds to indicate time stamps but should not contain milliseconds or errors will occur.</span></span>

<span data-ttu-id="a0b7a-p107">Ist der Vergleichsoperator "like", kann der Zeichenfolgenwert ein Sternchen (\*) enthalten, um nach einem oder mehreren Vorkommen eines beliebigen Zeichens oder einer beliebigen Teilzeichenfolge zu suchen. Bei einer Suche nach "state like 'M\*'" werden beispielsweise Maine und Massachusetts gefunden. Sie können auch führende und nachfolgende Sternchen verwenden, um nach einer Teilzeichenfolge innerhalb eines Werts zu suchen. Bei einer Suche nach "state like '\*as\*'" werden Alaska, Arkansas und Massachusetts gefunden.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-p107">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="a0b7a-p108">Sternchen können, wie oben dargestellt, nur am Ende oder nur am Anfang und am Ende einer \* -Zeichenfolge verwendet werden. Sie können das Sternchen nicht als führenden Platzhalter ('\*r') verwenden. In diesem Fall tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-p108">Asterisks can be used only at the end of a criteria string, or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str'), or embedded wildcard ('s\*r'). This will cause an error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a0b7a-p109">[!HINWEIS] Wird vor dem Aufrufen von <STRONG>Find</STRONG> keine aktuelle Zeilenposition festgelegt, tritt ein Fehler auf. Vor dem Aufrufen von <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Find</A> sollte eine beliebige Methode aufgerufen werden, die Zeilenpositionen festlegt (z. B. <STRONG>MoveFirst</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="a0b7a-p109">An error will occur if a current row position is not set before calling <STRONG>Find</STRONG>. Any method that sets row position, such as <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, should be called before calling <STRONG>Find</STRONG>.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="a0b7a-p110">[!HINWEIS] Wenn Sie die <STRONG>Find</STRONG> -Methode für einen Datensatz aufrufen und sich die aktuelle Position in der Datensatzgruppe beim letzten Datensatz oder am Ende der Datei (End of File, EOF) befindet, bleibt die Suche erfolglos. Sie müssen die <STRONG>MoveFirst</STRONG> -Methode aufrufen, um die aktuelle Position bzw. den Cursor auf den Anfang der Datensatzgruppe festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a0b7a-p110">If you call the <STRONG>Find</STRONG> method on a recordset, and the current position in the recordset is at the last record or end of file (EOF), you will not find anything. You need to call the <STRONG>MoveFirst</STRONG> method to set the current position/cursor to the beginning of the recordset.</span></span></P>


