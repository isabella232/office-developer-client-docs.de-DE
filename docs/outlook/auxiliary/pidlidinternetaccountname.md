---
title: PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5acca047-ff2a-716c-8dd4-b676fce1a3cf
description: Gibt den Anzeigenamen des Kontos zurück, das die Nachricht übermittelt hat.
ms.openlocfilehash: 2bd27cc7f868fb3f255a002ed70d0cb9b79516e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327685"
---
# <a name="pidlidinternetaccountname"></a>PidLidInternetAccountName

Gibt den Anzeigenamen des Kontos zurück, das die Nachricht übermittelt hat.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidInetAcctName  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Long-ID (Deckel):  <br/> |0x00008580  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft sollte den gleichen Wert enthalten, der von der Account Management API-Eigenschaft [PROP_ACCT_NAME](prop_acct_name.md) für das Konto zurückgegeben wird, das die Nachricht übermittelt hat. 
  
Nachrichtenspeicher Anbieter setzen diese benannte Eigenschaft und [pidlidinternetaccountstamp (](pidlidinternetaccountstamp.md) so fest, dass die folgenden Aktionen ausgeführt werden: 
  
- Wenn ein Benutzer auf **alle Antworten** in einer e-Mail-Nachricht klickt, entfernt Outlook die e-Mail-Adresse, die dem Konto zugeordnet ist, und wird auf die Nachricht aus der Empfängerliste der Antwort gestempelt. Dieses Verhalten tritt auf, es sei denn, diese e-Mail-Adresse ist der Absender der ursprünglichen Nachricht. 
    
- Standardmäßig sendet Outlook Antworten und weitergeleitete Nachrichten über das Konto, das auf die ursprüngliche Nachricht gestempelt ist.
    
In der Regel übermittelt der Outlook-Protokoll-Manager Nachrichten, und Outlook legt die Eigenschaften **pidlidinternetaccountname (** und **pidlidinternetaccountstamp (** fest, um das Konto anzugeben, das die Nachricht zugestellt hat. Wenn jedoch ein Nachrichtenspeicher eng mit einem Transport verbunden ist, stellt der Outlook-Protokoll-Manager keine Nachrichten bereit, und Outlook kann diese Eigenschaften nicht festlegen. In diesem Szenario ruft Outlook die [IMAPIProp:: GetIDsFromNames](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) -Funktion auf. Wenn der Nachrichtenspeicher Anbieter diese benannten Eigenschaften verfügbar machen möchte, sollte er **IMAPIProp:: GetIDsFromNames** implementieren und Eigenschaftstags über den Ausgabeparameter *lppPropTags* zurückgeben. Outlook kann dann die [IMAPIProp::](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) GetProps-Methode mithilfe dieser Eigenschaftstags aufrufen, und der Nachrichtenspeicher Anbieter kann den Kontonamen und den Stempel des gewünschten Kontos zurückgeben. 
  
Zur Unterstützung dieser benannten Eigenschaften sollten Speicheranbieter davon ausgehen, dass Outlook **IMAPIProp:: GetIDsFromNames** zum Abrufen des Eigenschaftentags für diese Eigenschaft verwendet. Outlook gibt die folgenden Werte für die [MAPINAMEID](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) -Struktur an, die dieser benannten Eigenschaft entspricht, die als Teil des Arrays übergeben wird, auf das durch den Eingabeparameter *lppPropNames* von **IMAPIProp:: GetIDsFromNames**verwiesen wird. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Art. lID:  <br/> |dispidInetAcctName  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md)
- [Konstanten (Account Management API)](constants-account-management-api.md)
- [Kanonische Pidlidinternetaccountname (-Eigenschaft](https://msdn.microsoft.com/library/29bedadf-903d-419d-804d-dc8bd92b745d%28Office.15%29.aspx)

