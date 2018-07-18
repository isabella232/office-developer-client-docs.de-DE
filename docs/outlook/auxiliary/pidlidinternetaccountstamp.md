---
title: PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 52003a4e-1b61-2965-5204-6601652dd15b
description: Gibt den Konto Zeitstempel für das Konto, das die Nachricht nicht übermittelt.
ms.openlocfilehash: ba54bffb60a05a3b4a1ff30519960740af93ebd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791175"
---
# <a name="pidlidinternetaccountstamp"></a>PidLidInternetAccountStamp

Gibt den Konto Zeitstempel für das Konto, das die Nachricht nicht übermittelt.
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidInetAcctStamp  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008581  <br/> |
|Datentyp:  <br/> |PT_UNICODE  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft sollte den gleichen Wert enthalten, der von der Konto-Verwaltungs-API-Eigenschaft [PROP_ACCT_STAMP](prop_acct_stamp.md) für das Konto zurückgegeben wird, die die Nachricht nicht übermittelt. 
  
Nachricht-Anbieter Bereitstellen dieser benannten Eigenschaft und [PidLidInternetAccountName](pidlidinternetaccountname.md) , so dass folgende Aktionen ausgeführt werden: 
  
- Wenn ein Benutzer **auf alle Antworten** in einer e-Mail-Nachricht klickt, entfernt Outlook die e-Mail-Adresse, die das Konto zugeordnet ist und für die Nachricht aus der Empfängerliste der Antwort versehen ist. Dieses Verhalten tritt auf, es sei denn, diese e-Mail-Adresse der Absender der ursprünglichen Nachricht ist. 
    
- Standardmäßig wird Outlook sendet Antworten und weitergeleitete Nachrichten über das Konto auf die ursprüngliche Nachricht versehen ist.
    
In der Regel die Outlook-Protokollmanager Nachrichten übermittelt, und Outlook legt die Eigenschaften **PidLidInternetAccountName** und **PidLidInternetAccountStamp** , um das Konto anzugeben, das die Nachricht nicht übermittelt. Wenn ein Nachrichtenspeichers eng mit einer Transport verknüpft ist, die Outlook-Protokollmanager übermittelt keine Nachrichten und Outlook diese Eigenschaften kann nicht festgelegt werden. In diesem Szenario ruft Outlook die [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) -Funktion. Wenn der Nachricht Speicheranbieter diese benannten Eigenschaften verfügbar zu machen möchte, muss **IMAPIProp::GetIDsFromNames** implementieren und Eigenschaftentags über die Ausgabe Parameter *LppPropTags* zurückzugeben. Outlook kann mithilfe dieser Eigenschaftentags dann die [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) -Methode aufrufen, und der Nachricht Speicheranbieter den Kontonamen und Zeitstempel für das gewünschte Konto zurückgeben. 
  
Zur Unterstützung der folgende benannten Eigenschaften erwarten Anbieter Outlook **IMAPIProp::GetIDsFromNames** verwendet, um das Eigenschafts-Tag für diese Eigenschaft abzurufen. Outlook gibt die folgenden Werte für die [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) -Struktur, die dieser benannten Eigenschaft entspricht, die als Teil des Arrays an, der input-Parameter *LppPropNames* des **IMAPIProp::GetIDsFromNames**auf zeigt übergeben wird. 
  
|||
|:-----|:-----|
|x LpGuid:  <br/> |PSETID_Common  <br/> |
|UlKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidInetAcctStamp  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Über die Konto-API](about-the-account-management-api.md) 
- [Konstanten (Account Management API)](constants-account-management-api.md)
- [PidLidInternetAccountStamp (kanonische Eigenschaft)](http://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)

