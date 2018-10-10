---
title: Command-Objekt - Übersicht
TOCTitle: Command Object Overview
ms:assetid: 3d6d81c4-4cf0-0c13-adb3-0c2c5934dc21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249166(v=office.15)
ms:contentKeyID: 48544346
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d1e6cd3b2ebea67fac7cef7e556038490b3eb9b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475805"
---
# <a name="command-object-overview"></a>Command-Objekt - Übersicht


**Betrifft**: Access 2013 | Office 2013

Die Auflistungen, Methoden und Eigenschaften eines **Command** -Objekts ermöglichen Folgendes:

  - Definieren des ausführbaren Texts des Befehls (z. B. eine SQL-Anweisung oder eine gespeicherte Prozedur) mithilfe der **CommandText** -Eigenschaft.

  - Definieren von parametrisierten Abfragen oder von Argumenten für gespeicherte Prozeduren mithilfe von **Parameter** -Objekten und der **Parameters** -Auflistung.

  - Ausführen eines Befehls und ggf. Zurückgeben eines **Recordset** -Objekts mithilfe der **Execute** -Methode.

  - Angeben des Befehlstyps mithilfe der **CommandType** -Eigenschaft vor der Ausführung, um die Leistung zu optimieren.

  - Steuern mithilfe der **Prepared** -Eigenschaft vor dem Ausführen, ob der Anbieter eine vorbereitete (oder kompilierte) Version des Befehls speichert.

  - Festlegen mithilfe der **CommandTimeout** -Eigenschaft, wie viele Sekunden ein Anbieter auf die Ausführung eines Befehls wartet.

  - Zuordnen einer geöffneten Verbindung zu einem **Command** -Objekt, indem dessen **ActiveConnection** -Eigenschaft festgelegt wird.

  - Festlegen der **Name** -Eigenschaft, um das **Command** -Objekt als Methode im zugeordneten **Connection** -Objekt zu identifizieren.

  - Übergeben eines **Command** -Objekts an die **Source** -Eigenschaft eines **Recordset** -Objekts, um Daten abzurufen.

