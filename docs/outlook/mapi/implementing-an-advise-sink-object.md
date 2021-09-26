---
title: Implementieren eines Advise-Senkenobjekts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b0873575cd06ca044364009785c9d87533cbad1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620750"
---
# <a name="implementing-an-advise-sink-object"></a>Implementieren eines Advise-Senkenobjekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann entweder eigene Empfehlungssenkenobjekte implementieren oder eine Hilfsprogrammfunktion, [HrAllocAdviseSink](hrallocadvisesink.md)verwenden. **HrAllocAdviseSink** erstellt ein "advise"-Senkenobjekt mit einer Implementierung von **"OnNotify",** die eine Rückruffunktion aufruft. 
  
Die Verwendung von **HrAllocAdviseSink** hat Vor- und Nachteile. Es kann Arbeit sparen, bietet jedoch keine Kontrolle über die Referenzzählung des von ihm erstellten Referenzsenkenobjekts. Daher sollten Clients, die die Freigabe ihrer Empfehlungssenke sorgfältig kontrollieren müssen oder gegenseitige Abhängigkeiten zwischen ihrem Empfehlungssenken und einem anderen Clientobjekt haben, eine eigene **IMAPIAdviseSink-Implementierung** erstellen und die Verwendung von **HrAllocAdviseSink** vermeiden. 
  
Ein Client, der eine eigene Empfehlungssenke implementiert, sollte es zu einem unabhängigen Objekt machen, das nicht mit anderen Objekten in Zusammenhang steht oder von diesen abhängig ist, um potenzielle Komplikationen bei der Referenzzählung und Objektfreigabe zu vermeiden. Wenn Sie jedoch die Empfehlungssenke als Teil eines anderen Objekts implementieren oder einen Rückwärtszeiger auf ein anderes Objekt als Datenelement einschließen müssen, wird empfohlen, dass zwei separate Verweisanzahlen beibehalten werden: eine für das Objekt, auf das von der Empfehlungssenke verwiesen wird, und eine für die Empfehlungssenke. 
  
Wenn die Referenzanzahl des referenzierten Objekts auf Null fällt, können alle zugehörigen Methoden fehlschlagen, und die vtable kann zerstört werden, aber der Speicher für die Empfehlungssenke muss intakt bleiben, bis die Referenzanzahl ebenfalls auf Null fällt. Dies bedeutet, dass die **Release-Methode** der Empfehlungssenke die Referenzanzahl verringert und die Zerstörung des Objekts beenden muss, wenn diese Anzahl Null erreicht. Wenn zwei separate Verweisanzahlen nicht beibehalten werden, wäre es einfach, versehentlich die Empfehlungssenke im Rahmen des **Release-Prozesses** des umfassenden Objekts zu zerstören. 
  
Clients, **die HrAllocAdviseSink** zum Implementieren einer Empfehlungssenke verwenden, müssen ebenso vorsichtig sein, ihre Rückruffunktion nicht als Methode in ein anderes Empfehlungssenkenobjekt einzuschließen. Für C++-Clients ist es verlockend, dies zu tun und  _diesen_ Zeiger als Parameter zu übergeben. Dies ist eine gefährliche Strategie, da Clients in der Regel ein Objekt freigeben, wenn dessen Referenzanzahl Null erreicht. Das Freigeben des Speichers für das Empfehlungssenkenobjekt würde  _diesen_ Zeiger ungültig machen. 
  
Abhängig vom Ereignistyp und der Empfehlungsquelle kann Ihre **OnNotify-Methode** Ereignisse auf verschiedene Arten behandeln. Die folgende Tabelle enthält Vorschläge zum Behandeln einiger Standardereignisse. 
  
|**Ereignistyp**|**Behandeln in OnNotify**|
|:-----|:-----|
|Objekt verschoben  <br/> |Wenn das ursprüngliche übergeordnete Objekt des verschobenen Objekts mit dem neuen übergeordneten Objekt verknüpft ist, aktualisieren Sie die Ansicht beginnend mit dem Ordner oder Adressbuchcontainer, der in der Hierarchie am höchsten ist. Wenn die beiden übergeordneten Container nicht verbunden sind, aktualisieren Sie beide Ansichten.  <br/> |
|Neue Nachricht  <br/> |Ändern Sie die Benutzeroberfläche, um den Benutzer über das Eintreffen einer oder mehrerer neuer Nachrichten zu informieren. Platzieren Sie den Empfangsordner in der aktuellen Ansicht.  <br/> |
|Fehler  <br/> |Protokollieren Sie den Fehler bei Bedarf für alle Objekte mit Ausnahme der Sitzung, und geben Sie den Fehler zurück. Melden Sie sich für das Sitzungsobjekt nach Möglichkeit ab.  <br/> |
|Suche abgeschlossen  <br/> |Keine Verarbeitung erforderlich.  <br/> |
   
> [!NOTE]
> Benachrichtigungshandler sollten erneut reaktiviert werden. 
  

