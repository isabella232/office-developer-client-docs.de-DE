---
title: Unterstützung der formatierte Text Nachrichtenspeicher Zuständigkeiten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 301ebbf8e7a3e2a2deb303af5b198fd11511d495
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795649"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>Unterstützung von formatiertem Text: Aufgaben des Nachrichtenspeichers

  
  
**Betrifft**: Outlook 
  
Nachricht Speicheranbieter verwenden Sie die Eigenschaft **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) um zu veröffentlichen, und zwar unabhängig davon, ob sie HTML-Text: Rich Text Format (RTF) verarbeitet werden können und, falls sie RTF-fähigen sind, ob das Speichern von formatierten Texts in ein komprimierte oder nicht komprimierten Format. Nachricht Anbieter anzugeben, dass sie RTF-fähigen sind, indem Sie die STORE_RTF_OK Bit und sie den formatierten Text in einen nicht komprimierten Format speichern, indem Sie das STORE_UNCOMPRESSED_RTF Bit. Nachricht Anbieter geben Sie an, dass sie HTML-fähigen sind, indem Sie die STORE_HTML_OK Bit.
  
Es ist, zwar wichtig für ein RTF-fähigen Client zu prüfen, ob die STORE_RTF_OK bit, um zu bestimmen, ob ein Nachrichtenspeichers RTF unterstützt ist es nicht erforderlich, damit ein Client mit dem Format des formatierten Text ein RTF-fähigen Store betreffenden werden. 
  
Alle Nachrichtenspeicher müssen nicht-RTF-fähigen Clients unterstützen. Ein Nachrichtenspeicher ohne RTF-Unterstützung muss die **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))-Eigenschaft während eines Anrufs an die Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode löschen, wenn ein Client ohne **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) geändert hat Aktualisieren von **PR_RTF_IN_SYNC** oder **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). Löschen von **PR_RTF_IN_SYNC** bewirkt, dass die **PR_RTF_COMPRESSED** -Eigenschaft von der **PR_BODY** -Eigenschaft das nächste Mal neu berechnet werden, das ein RTF-fähigen Client [RTFSync](rtfsync.md)aufruft. 
  
Die meisten RTF-fähigen Nachrichtenspeicher erhalten den Nachrichtentext nicht von Clients; Es muss auf Anforderung berechnet werden. Da diese Berechnung zeitaufwändig und kostspielig ist, sollten Clients **PR_RTF_COMPRESSED** möglichst verwenden. Um die **PR_BODY** -Eigenschaft zu berechnen, muss der Nachricht Speicheranbieter Dekomprimieren Sie die Inhalte der Eigenschaft **PR_RTF_COMPRESSED** und entfernt die rich-Text-Formatierung. Clients, die nicht die **PR_RTF_COMPRESSED** -Eigenschaft unterstützen müssen diese Berechnung stattfinden für jede Nachricht. 
  
Beim Kopieren von Nachrichten speichern Nachricht Anbieter, die die **IMAPISupport::DoCopyProps** oder **IMAPISupport::DoCopyTo** -Methoden, die das Risiko eine Nachricht ohne Inhalt erstellen, wenn ihre Implementierung der **PR_BODY** schließt nicht verwenden Eigenschaft und **PR_RTF_COMPRESSED**nutzt. Es ist möglich, für die Daten in der Eigenschaft **PR_RTF_COMPRESSED** beschädigt. Vor dem Ausschluss eines dieser Nachricht von Eigenschaften in den Kopiervorgang, überprüfen Sie eine Beschädigung wie folgt: 
  
1. Ist der Wert der **PR_RTF_COMPRESSED** nicht größer als die komprimierte RTF, ist beschädigt. 
    
2. Wenn der magische Wert im RTF-Header nicht _DwMagicCompressedRTF_ oder _DwMagicUncompressedRTF_, die Eigenschaft ist beschädigt.
    
Nachrichtenspeicher Anbieter mit Unterstützung des benötigten Methoden nicht betroffenen mit implementieren eine Prüfung **PR_RTF_COMPRESSED** Beschädigung werden; MAPI wird sichergestellt, dass die entsprechenden Eigenschaften vorhanden und gültig sind. 
  
Es gibt drei verschiedene Ebenen von RTF-Unterstützung Nachricht-Anbieter implementiert werden können. MAPI empfiehlt, RTF-fähigen Nachricht-Anbieter die Unterstützung der mittleren oder höchste Ebene implementieren. Alle RTF-fähigen Nachrichtenspeicher Anbieter übernehmen generieren **PR_BODY** aus die Daten in **PR_RTF_COMPRESSED** für ausgehende Nachrichten enthalten, und rufen Sie **RTFSync** zum Synchronisieren von Text und Formatierung für eingehende Nachrichten. 
  
In der folgenden Tabelle werden die Unterschiede zwischen diesen drei Ebenen beschrieben. 
  
|**Unterstützungsumfang**|**Beschreibung**|
|:-----|:-----|
|Low  <br/> |Nachricht Aufrufe eines **RTFSync** speichern, wenn Änderungen auf eine Nachricht gespeichert werden und extrahiert die Daten für die Eigenschaft **PR_BODY** aus **PR_RTF_COMPRESSED** statt erfordern Clients festgelegt. **PR_BODY** und **PR_RTF_COMPRESSED** werden gespeichert.  <br/> |
|Mitte  <br/> |Nachrichtenspeicher Anbieter speichert nur die **PR_RTF_COMPRESSED** -Eigenschaft, Netzwerke **PR_BODY** bei Bedarf.  <br/> |
|High  <br/> |Nachrichtenspeicher Anbieter Speicher weder **PR_BODY** oder die Hilfs RTF-Eigenschaften. **RTFSync** wird aufgerufen, wenn der Nachrichtentext geändert wurde und die Formatierung unverändert bleibt oder eine neue Nachricht von eines Transportdienstes heruntergeladen wird.  <br/> |
   

