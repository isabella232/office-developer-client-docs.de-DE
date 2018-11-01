---
title: Command-Objekt - Übersicht
TOCTitle: Command Object Overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39724156b8644b6d99ffec82bdf79624b6cfaee1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875035"
---
# <a name="command-object-overview"></a><span data-ttu-id="60c57-102">Command-Objekt - Übersicht</span><span class="sxs-lookup"><span data-stu-id="60c57-102">Command Object Overview</span></span>


<span data-ttu-id="60c57-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60c57-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60c57-104">Die Auflistungen, Methoden und Eigenschaften eines **Command** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="60c57-104">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="60c57-105">Definieren des ausführbaren Texts des Befehls (z. B. eine SQL-Anweisung oder eine gespeicherte Prozedur) mithilfe der **CommandText** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="60c57-105">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the **CommandText** property.</span></span>

  - <span data-ttu-id="60c57-106">Definieren von parametrisierten Abfragen oder von Argumenten für gespeicherte Prozeduren mithilfe von **Parameter** -Objekten und der **Parameters** -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="60c57-106">Define parameterized queries or stored procedure arguments by using **Parameter** objects and the **Parameters** collection.</span></span>

  - <span data-ttu-id="60c57-107">Ausführen eines Befehls und ggf. Zurückgeben eines **Recordset** -Objekts mithilfe der **Execute** -Methode.</span><span class="sxs-lookup"><span data-stu-id="60c57-107">Execute a command and return a **Recordset** object, if appropriate, by using the **Execute** method.</span></span>

  - <span data-ttu-id="60c57-108">Angeben des Befehlstyps mithilfe der **CommandType** -Eigenschaft vor der Ausführung, um die Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="60c57-108">Specify the type of command by using the **CommandType** property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="60c57-109">Steuern mithilfe der **Prepared** -Eigenschaft vor dem Ausführen, ob der Anbieter eine vorbereitete (oder kompilierte) Version des Befehls speichert.</span><span class="sxs-lookup"><span data-stu-id="60c57-109">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the **Prepared** property.</span></span>

  - <span data-ttu-id="60c57-110">Festlegen mithilfe der **CommandTimeout** -Eigenschaft, wie viele Sekunden ein Anbieter auf die Ausführung eines Befehls wartet.</span><span class="sxs-lookup"><span data-stu-id="60c57-110">Set the number of seconds that a provider will wait for a command to execute by using the **CommandTimeout** property.</span></span>

  - <span data-ttu-id="60c57-111">Zuordnen einer geöffneten Verbindung zu einem **Command** -Objekt, indem dessen **ActiveConnection** -Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="60c57-111">Associate an open connection with a **Command** object by setting its **ActiveConnection** property.</span></span>

  - <span data-ttu-id="60c57-112">Festlegen der **Name** -Eigenschaft, um das **Command** -Objekt als Methode im zugeordneten **Connection** -Objekt zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="60c57-112">Set the **Name** property to identify the **Command** object as a method on the associated **Connection** object.</span></span>

  - <span data-ttu-id="60c57-113">Übergeben eines **Command** -Objekts an die **Source** -Eigenschaft eines **Recordset** -Objekts, um Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="60c57-113">Pass a **Command** object to the **Source** property of a **Recordset** in order to obtain data.</span></span>

