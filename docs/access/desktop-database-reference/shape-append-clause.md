---
title: Shape Append-Klausel
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40c35e8b2c3fb3f0b92bf261b62c252a61a367b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306447"
---
# <a name="shape-append-clause"></a><span data-ttu-id="b9d00-102">Shape Append-Klausel</span><span class="sxs-lookup"><span data-stu-id="b9d00-102">Shape Append clause</span></span>


<span data-ttu-id="b9d00-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9d00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9d00-p101">The shape command APPEND clause appends a column or columns to a **Recordset**. Often these columns are chapter columns, which refer to a child **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="b9d00-p101">The shape command APPEND clause appends a column or columns to a **Recordset**. Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9d00-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9d00-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="b9d00-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9d00-107">Description</span></span>

<span data-ttu-id="b9d00-108">Die Teile dieser Klausel lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b9d00-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="b9d00-109">*parent-command*</span><span class="sxs-lookup"><span data-stu-id="b9d00-109">*parent-command*</span></span>

- <span data-ttu-id="b9d00-110">Keiner oder einer der Folgenden (Sie können *parent-command* ganz weglassen):</span><span class="sxs-lookup"><span data-stu-id="b9d00-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="b9d00-p102">Ein Anbieterbefehl in geschweiften Klammern ("{}"), der ein **Recordset** -Objekt zurückgibt. Der Befehl wird an den zugrunde liegenden Datenprovider ausgegeben, und die Syntax hängt von den Anforderungen dieses Anbieters ab. Normalerweise handelt es sich dabei um die SQL-Sprache, obwohl für ADO keine bestimmte Abfragesprache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b9d00-p102">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="b9d00-114">Another shape command embedded in parentheses.</span><span class="sxs-lookup"><span data-stu-id="b9d00-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="b9d00-115">Das TABLE-Schlüsselwort, gefolgt vom Namen einer Tabelle im Datenprovider.</span><span class="sxs-lookup"><span data-stu-id="b9d00-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="b9d00-116">*parent-alias*</span><span class="sxs-lookup"><span data-stu-id="b9d00-116">*parent-alias*</span></span>

  - <span data-ttu-id="b9d00-117">Ein optionaler Alias, das auf das übergeordnete **Recordset** -Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="b9d00-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="b9d00-118">*column-list*</span><span class="sxs-lookup"><span data-stu-id="b9d00-118">*column-list*</span></span>

  - <span data-ttu-id="b9d00-119">Mindestens eines der Folgenden:</span><span class="sxs-lookup"><span data-stu-id="b9d00-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="b9d00-120">Eine Aggregatspalte.</span><span class="sxs-lookup"><span data-stu-id="b9d00-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="b9d00-121">Eine berechnete Spalte.</span><span class="sxs-lookup"><span data-stu-id="b9d00-121">A calculated column.</span></span>
    
    - <span data-ttu-id="b9d00-122">Eine neue Spalte, die mit der NEW-Klausel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b9d00-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="b9d00-p103">Eine Kapitelspalte. Eine Kapitelspaltendefinition wird in Klammern ("()") eingeschlossen. Siehe nachstehende Syntax:</span><span class="sxs-lookup"><span data-stu-id="b9d00-p103">A chapter column. A chapter column definition is enclosed in parentheses ("()"). See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="b9d00-126">*child-recordset*</span><span class="sxs-lookup"><span data-stu-id="b9d00-126">*child-recordset*</span></span>

  - <span data-ttu-id="b9d00-p104">Ein Anbieterbefehl in geschweiften Klammern ("{}"), der ein **Recordset** -Objekt zurückgibt. Der Befehl wird an den zugrunde liegenden Datenprovider ausgegeben, und die Syntax hängt von den Anforderungen dieses Anbieters ab. Normalerweise handelt es sich dabei um die SQL-Sprache, obwohl für ADO keine bestimmte Abfragesprache erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b9d00-p104">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="b9d00-130">Another shape command embedded in parentheses.</span><span class="sxs-lookup"><span data-stu-id="b9d00-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="b9d00-131">Der Name eines vorhandenen geformten **Recordset**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="b9d00-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="b9d00-132">Das TABLE-Schlüsselwort, gefolgt vom Namen einer Tabelle im Datenprovider.</span><span class="sxs-lookup"><span data-stu-id="b9d00-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="b9d00-133">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="b9d00-133">*child-alias*</span></span>

  - <span data-ttu-id="b9d00-134">Ein Alias, der auf das untergeordnete **Recordset** -Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="b9d00-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="b9d00-135">*parent-column*</span><span class="sxs-lookup"><span data-stu-id="b9d00-135">*parent-column*</span></span>

  - <span data-ttu-id="b9d00-136">Eine Spalte im **Recordset**-Objekt, die von *parent-command* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b9d00-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="b9d00-137">*child-column*</span><span class="sxs-lookup"><span data-stu-id="b9d00-137">*child-column*</span></span>

  - <span data-ttu-id="b9d00-138">Eine Spalte im **Recordset**-Objekt, die von *child-command* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b9d00-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="b9d00-139">*param-number*</span><span class="sxs-lookup"><span data-stu-id="b9d00-139">*param-number*</span></span>

  - <span data-ttu-id="b9d00-140">Siehe [Verwenden von parametrisierten Befehlen](operation-of-parameterized-commands.md).</span><span class="sxs-lookup"><span data-stu-id="b9d00-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="b9d00-141">*chapter-alias*</span><span class="sxs-lookup"><span data-stu-id="b9d00-141">*chapter-alias*</span></span>

  - <span data-ttu-id="b9d00-142">Ein Alias, der auf die dem übergeordneten Element angefügte Kapitelspalte verweist.</span><span class="sxs-lookup"><span data-stu-id="b9d00-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="b9d00-143">Die _"Parent-column to child-column"_ -Klausel ist tatsächlich eine Liste, in der jede definierte Beziehung durch ein Komma getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="b9d00-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="b9d00-144">Die Klausel hinter dem APPEND-Schlüsselwort ist tatsächlich eine Liste, in der die einzelnen Klauseln durch ein Komma getrennt werden und eine weitere Spalte definiert wird, die der übergeordneten Spalte angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9d00-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="b9d00-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9d00-145">Remarks</span></span>

<span data-ttu-id="b9d00-p105">Wenn Sie Anbieterbefehle aus Benutzereingaben als Teil eines SHAPE-Befehls erstellen, wird der vom Benutzer bereitgestellte Anbieterbefehl von SHAPE als undurchsichtige Zeichenfolge behandelt und originalgetreu dem Anbieter übergeben. Beispielsweise werden im folgenden SHAPE-Befehl</span><span class="sxs-lookup"><span data-stu-id="b9d00-p105">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider. For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="b9d00-148">SHAPE führt zwei Befehle aus: wählen \* Sie von T1 aus, \* und wählen Sie aus T2 Beziehung K1 zu K2 aus.</span><span class="sxs-lookup"><span data-stu-id="b9d00-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="b9d00-149">Wenn der Benutzer einen Verbundbefehl bereitstellt, der aus mehreren durch Semikolons getrennten Anbieterbefehlen besteht, wird der Unterschied von SHAPE nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="b9d00-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="b9d00-150">Im folgenden SHAPE-Befehl</span><span class="sxs-lookup"><span data-stu-id="b9d00-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="b9d00-151">Form führt Auswahl \* aus T1 aus; DROP TABLE T1 and (Select \* from T2 Relate K1 to K2), nicht erkennen, dass DROP TABLE T1 ein separates und in diesem Fall ein gefährlicher, Anbieterbefehl ist.</span><span class="sxs-lookup"><span data-stu-id="b9d00-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="b9d00-152">Die Benutzereingabe muss von Anwendungen immer überprüft werden, um derartige potenzielle Hackerangriffe zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="b9d00-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>

<span data-ttu-id="b9d00-153">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b9d00-153">This section includes the following topics:</span></span>

- [<span data-ttu-id="b9d00-154">Betrieb von nicht parametrisierten Befehlen</span><span class="sxs-lookup"><span data-stu-id="b9d00-154">Operation of Non-Parameterized Commands</span></span>](operation-of-non-parameterized-commands.md)

- [<span data-ttu-id="b9d00-155">Betrieb von parametrisierten Befehlen</span><span class="sxs-lookup"><span data-stu-id="b9d00-155">Operation of Parameterized Commands</span></span>](operation-of-parameterized-commands.md)

- [<span data-ttu-id="b9d00-156">Hybrid Befehle</span><span class="sxs-lookup"><span data-stu-id="b9d00-156">Hybrid Commands</span></span>](hybrid-commands.md)

- [<span data-ttu-id="b9d00-157">Dazwischenliegende Shape COMPUTE-Klauseln</span><span class="sxs-lookup"><span data-stu-id="b9d00-157">Intervening Shape COMPUTE Clauses</span></span>](intervening-shape-compute-clauses.md)
