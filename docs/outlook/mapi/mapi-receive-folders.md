---
title: MAPI empfangen Ordner
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e1287a3-0f15-4d9a-b7ee-738fce9cd51f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 619bd2d5e3b40e49da835d774035ba237af06699
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793047"
---
# <a name="mapi-receive-folders"></a>MAPI empfangen Ordner

  
  
**Betrifft**: Outlook 
  
Eine Empfangsordner enth�lt eingehende Nachrichten von einer bestimmten Nachrichtenklasse. Empfangsordner, die Zuordnungen von Clients, vom Anbieter Store Nachricht oder MAPI hergestellt werden k�nnen. MAPI hat zwei Standard Ordner empfangen: im Stammordner des Nachrichtenspeichers und den Ordner Posteingang des untergeordneten Baumes zwischen Personen Nachricht (IPM). Der Stammordner des Nachrichtenspeichers ist die Standardeinstellung Empfangsordner f�r alle prozess�bergreifenden Kommunikation (IPK) Nachrichten.
  
 Der Ordner Posteingang wird vom MAPI f�r alle neuen Nachrichtenspeicher erstellt und agiert als Standard Empfangsordner f�r die folgenden Nachrichtenklassen: 
  
- Die Nachrichtenklasse IPM.
    
- Die Nachrichtenklasse des Berichts.
    
- Eine leere oder fehlende,-Klasse.
    
Alle Berichtnachrichten, auch wenn diese als Antwort auf eine Nachricht IPK gesendet werden im Ordner Posteingang platziert. IPK-Clientanwendungen, die ihre eigenen Berichte verarbeiten m�ssen explizit eine Empfangsordner f�r die Klasse des Berichts hinzuf�gen. Wenn beispielsweise ein Client erwartet, zum Empfangen von Nachrichten mit der IPK-Klasse. Paper.Order, sollten sie die [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) -Methode zum Herstellen einer Empfangsordner f�r Berichte mit der Report.IPC.Paper.Order-Klasse aufrufen. 
  
Erhalten Sie Ordner, den Zuordnungen f�r die hierarchische Organisation von Nachrichtenklassen basieren. Clients k�nnen explizit eine Zuordnung zwischen einem Empfangsordner und eine Nachrichtenklasse herstellen oder verwenden Sie die MAPI-Standardordner empfangen. Festlegen von Clients in der Regel ein Ordner zum Empfangen von Nachrichten f�r eine Basisklasse und alle Unterklassen. Beispielsweise w�rde ein typischer Client eine Zuordnung f�r Nachrichten mit der Klasse **MyClass**herstellen. Wenn der Client Nachrichten mit Klassen **MyClass.Home** oder **MyClass.Home.Kitchen.Computer**empfangen, w�rde dann diese Nachrichten den Empfangsordner f�r die Basisklasse **MyClass**�ffnen.
  
Es gibt drei Nachricht, dass Store-Methoden, mit denen Clients zum Arbeiten mit Ordnern erhalten:
  
- [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)
    
- [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)
    
- [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)
    
Die Ordner-Tabelle ist eine Auflistung von Informationen �ber alle empfangen Ordner f�r einen Nachrichtenspeicher hergestellt. Festgelegter erforderliche Spalte enth�lt die Nachrichtenklasse sowie die Datensatzschl�ssel und die Eintrags-ID an.
  
To retrieve a receive folder for a particular message class, clients pass the message class string to the [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) method. The message store provider returns an entry identifier for the corresponding folder. To implement **GetReceiveFolder**, a message store provider should use an algorithm that selects the folder whose associated message class matches the longest possible prefix of the specified message class. For example, assume the message store has the following associations between receive folders and message classes in its receive folder table:
  
- **IPM** Nachrichten werden im Ordner Posteingang abgelegt. 
    
- **IPM.Note.Sample** Nachrichten befinden sich im Ordner Samples. 
    
Die folgende Tabelle zeigt, wie Nachrichten mit verschiedenen Klassen an die entsprechende weitergeleitet werden w�rde, Empfangsordner.
  
|**Eingehende Nachricht-Klasse**|**Ordner empfangen**|
|:-----|:-----|
|**IPM. Note.Sample.Simple** <br/> |F�r Beispielordner  <br/> |
|**IPM. Hinweis** <br/> |Ordner Posteingang  <br/> |
|**IPM. Zeitkarte** <br/> |Ordner Posteingang  <br/> |
|**IPM. Note.Sample.Simple.Totally** <br/> |F�r Beispielordner  <br/> |
   
Clients rufen Sie die **SetReceiveFolder** -Methode, um eine explizite Zuordnung zwischen einem bestimmten Nachrichtenklasse t�tigen und annehmen von Ordner. Wenn eine Nachricht an eine leere Nachrichtenklasse �bermittelt werden, platziert MAPI die Nachricht im Ordner "empfangen", die f�r ein Pr�fix der leere-Klasse definiert ist. Wenn der Client eine Empfangsordner f�r Nachrichten mit Klasse **IPM** hergestellt hat und eine Nachricht mit der Klasse **IPM.Note.Test** �bermittelt wird, wird diese Nachricht im Ordner "empfangen" f�r die Nachrichtenklasse **IPM** platziert. 
  
Clients in der Regel eine Meldungszeichenfolge-Klasse �bergeben, und klicken Sie in das **SetReceiveFolder**aufrufen, die Eintrags-ID des neuen Ordner empfangen. Clients k�nnen jedoch NULL f�r eine oder beide der folgenden Parameter �bergeben. Die folgende Tabelle beschreibt das Verhalten, das ergibt NULL f�r die Nachricht-Klasse und Eintrags-ID-Parameter angeben. 
  
|**_SetReceiveFolder_ -parameter**|**Resultierende Verhalten**|
|:-----|:-----|
|Eintrags-ID auf NULL festgelegt wurde  <br/> |Nachrichtenspeicher l�scht die Zuordnung zwischen dem angegebenen-Klasse und die vorhandene Ordner empfangenen Nachricht. Empfangen einer neuen Ordner ist nicht hergestellt werden. <br/> Nachfolgende Aufrufe von **GetReceiveFolder** mit dieser Nachrichtenklasse gibt den Empfangsordner f�r ein Pr�fix der Nachrichtenklasse zur�ck. f�r neue Nachrichtenspeicher werden **GetReceiveFolder** Posteingang IPM-Unterstruktur zur�ckgegeben.    <br/> |
|Nachrichtenklasse auf NULL festgelegt wurde  <br/> |Nachrichtenspeicher �ndert die Zuordnung f�r die leere Nachrichtenklasse in den angegebenen Ordner. In diesem Ordner gehen eingehende Nachrichten, deren Klasse andernfalls nicht erkannt wird.  <br/> |
|Eintrags-ID und die Nachrichtenklasse auf NULL festgelegt wurde  <br/> |Nachrichtenspeicher l�scht die Zuordnung Klasse-Ordner f�r die Nachrichtenklasse leer. Sie sollten nicht beide Parameter auf NULL festgelegt, da sich daraus in der Regel eingehende Nachrichten in den Stammordner des Nachrichtenspeichers, einen Ordner, der an den Client nicht sichtbar ist platziert wird.  <br/> |
   
Auch wenn eine Nachricht Klasse niemals leer sein sollte, kann ein leerer Nachrichtenklasse auftreten. Der Nachrichtenspeicher Verantwortung **IPM** f�r neue ausgehende Nachrichten, die eine leere Klasse haben die Nachrichtenklasse zugewiesen ist. Es ist der Adressbuchhierarchie Verantwortung zuweisen **IPM.Note** wie die-Klasse f�r eingehende Nachrichten, die alle leere Klasse aufweisen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Ordner](mapi-folders.md)

