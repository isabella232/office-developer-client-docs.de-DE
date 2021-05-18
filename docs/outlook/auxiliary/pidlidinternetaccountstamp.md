---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Gibt den Kontostempel des Kontos zurück, das die Nachricht übermittelt hat.
ms.openlocfilehash: c5da45268cefbe09588fdcfcda32e4e7a4be9d5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327727"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

Gibt den Kontostempel des Kontos zurück, das die Nachricht übermittelt hat.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidInetAcctStamp  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Common  <br/> |
|Lange ID (LID):  <br/> |0x00008581  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft sollte denselben Wert enthalten, der von der Account Management-API-Eigenschaft [PROP_ACCT_STAMP](prop_acct_stamp.md) für das Konto zurückgegeben wird, das die Nachricht übermittelt hat. 
  
Nachrichtenspeicheranbieter machen diese benannte Eigenschaft und [PidLidInternetAccountName](pidlidinternetaccountname.md) verfügbar, sodass die folgenden Aktionen auftreten: 
  
- Wenn ein Benutzer **in** einer E-Mail auf Alle antworten klickt, entfernt Outlook die E-Mail-Adresse, die dem Konto zugeordnet ist, und wird in der Nachricht aus der Empfängerliste der Antwort gestempelt. Dieses Verhalten tritt auf, es sei denn, diese E-Mail-Adresse ist der Absender der ursprünglichen Nachricht. 
    
- Standardmäßig sendet Outlook Antworten und weitergeleitete Nachrichten über das Konto, das in der ursprünglichen Nachricht gestempelt ist.
    
Normalerweise stellt der Outlook-Protokoll-Manager Nachrichten zu, und Outlook legt die **Eigenschaften PidLidInternetAccountName** und **PidLidInternetAccountStamp** fest, um das Konto anzugeben, das die Nachricht übermittelt hat. Wenn ein Nachrichtenspeicher jedoch eng mit einem Transport gekoppelt ist, liefert der Outlook-Protokoll-Manager keine Nachrichten, und Outlook eigenschaften können nicht festgelegt werden. In diesem Szenario wird Outlook [IMAPIProp::GetIDsFromNames-Funktion](https://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) aufruft. Wenn der Nachrichtenspeicheranbieter diese benannten Eigenschaften verfügbar machen möchte, sollte er **IMAPIProp::GetIDsFromNames** implementieren und Eigenschaftstags über den Ausgabeparameter *lppPropTags zurückgeben.* Outlook können dann die [IMAPIProp::GetProps-Methode](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) mithilfe dieser Eigenschaftstags aufrufen, und der Nachrichtenspeicheranbieter kann den Kontonamen und den Stempel des gewünschten Kontos zurückgeben. 
  
Zur Unterstützung dieser benannten Eigenschaften sollten Speicheranbieter erwarten, dass Outlook **IMAPIProp::GetIDsFromNames** verwendet, um das Eigenschaftstag für diese Eigenschaft zu erhalten. Outlook gibt die folgenden Werte für die [MAPINAMEID-Struktur](https://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) an, die dieser benannten Eigenschaft entspricht, die als Teil des Arrays übergeben wird, auf das der Eingabeparameter *lppPropNames* von **IMAPIProp::GetIDsFromNames** verweist. 
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctStamp  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)
- [PidLidInternetAccountStamp (kanonische Eigenschaft)](https://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

