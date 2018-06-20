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
# <a name="pidlidinternetaccountstamp"></a><span data-ttu-id="661a1-103">PidLidInternetAccountStamp</span><span class="sxs-lookup"><span data-stu-id="661a1-103">PidLidInternetAccountStamp</span></span>

<span data-ttu-id="661a1-104">Gibt den Konto Zeitstempel für das Konto, das die Nachricht nicht übermittelt.</span><span class="sxs-lookup"><span data-stu-id="661a1-104">Returns the account stamp of the account that delivered the message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="661a1-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="661a1-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="661a1-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="661a1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="661a1-107">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="661a1-107">dispidInetAcctStamp</span></span>  <br/> |
|<span data-ttu-id="661a1-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="661a1-108">Property set:</span></span>  <br/> |<span data-ttu-id="661a1-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="661a1-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="661a1-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="661a1-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="661a1-111">0x00008581</span><span class="sxs-lookup"><span data-stu-id="661a1-111">0x00008581</span></span>  <br/> |
|<span data-ttu-id="661a1-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="661a1-112">Data type:</span></span>  <br/> |<span data-ttu-id="661a1-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="661a1-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="661a1-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="661a1-114">Area:</span></span>  <br/> |<span data-ttu-id="661a1-115">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="661a1-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="661a1-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="661a1-116">Remarks</span></span>

<span data-ttu-id="661a1-117">Diese Eigenschaft sollte den gleichen Wert enthalten, der von der Konto-Verwaltungs-API-Eigenschaft [PROP_ACCT_STAMP](prop_acct_stamp.md) für das Konto zurückgegeben wird, die die Nachricht nicht übermittelt.</span><span class="sxs-lookup"><span data-stu-id="661a1-117">This property should contain the same value that is returned from the Account Management API property [PROP_ACCT_STAMP](prop_acct_stamp.md) for the account that delivered the message.</span></span> 
  
<span data-ttu-id="661a1-118">Nachricht-Anbieter Bereitstellen dieser benannten Eigenschaft und [PidLidInternetAccountName](pidlidinternetaccountname.md) , so dass folgende Aktionen ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="661a1-118">Message store providers expose this named property and [PidLidInternetAccountName](pidlidinternetaccountname.md) so that the following actions occur:</span></span> 
  
- <span data-ttu-id="661a1-119">Wenn ein Benutzer **auf alle Antworten** in einer e-Mail-Nachricht klickt, entfernt Outlook die e-Mail-Adresse, die das Konto zugeordnet ist und für die Nachricht aus der Empfängerliste der Antwort versehen ist.</span><span class="sxs-lookup"><span data-stu-id="661a1-119">When a user clicks **Reply to All** in an email message, Outlook removes the email address that is associated with the account and is stamped on the message from the recipient list of the reply.</span></span> <span data-ttu-id="661a1-120">Dieses Verhalten tritt auf, es sei denn, diese e-Mail-Adresse der Absender der ursprünglichen Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="661a1-120">This behavior occurs unless this email address is the sender of the original message.</span></span> 
    
- <span data-ttu-id="661a1-121">Standardmäßig wird Outlook sendet Antworten und weitergeleitete Nachrichten über das Konto auf die ursprüngliche Nachricht versehen ist.</span><span class="sxs-lookup"><span data-stu-id="661a1-121">By default, Outlook sends replies and forwarded messages through the account that is stamped on the original message.</span></span>
    
<span data-ttu-id="661a1-122">In der Regel die Outlook-Protokollmanager Nachrichten übermittelt, und Outlook legt die Eigenschaften **PidLidInternetAccountName** und **PidLidInternetAccountStamp** , um das Konto anzugeben, das die Nachricht nicht übermittelt.</span><span class="sxs-lookup"><span data-stu-id="661a1-122">Usually, the Outlook Protocol Manager delivers messages, and Outlook sets the **PidLidInternetAccountName** and **PidLidInternetAccountStamp** properties to indicate the account that delivered the message.</span></span> <span data-ttu-id="661a1-123">Wenn ein Nachrichtenspeichers eng mit einer Transport verknüpft ist, die Outlook-Protokollmanager übermittelt keine Nachrichten und Outlook diese Eigenschaften kann nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="661a1-123">However, if a message store is tightly coupled with a transport, the Outlook Protocol Manager does not deliver messages and Outlook cannot set these properties.</span></span> <span data-ttu-id="661a1-124">In diesem Szenario ruft Outlook die [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="661a1-124">In this scenario, Outlook calls the [IMAPIProp::GetIDsFromNames](http://msdn.microsoft.com/library/e3f501a4-a8ee-43d7-bd83-c94e7980c398%28Office.15%29.aspx) function.</span></span> <span data-ttu-id="661a1-125">Wenn der Nachricht Speicheranbieter diese benannten Eigenschaften verfügbar zu machen möchte, muss **IMAPIProp::GetIDsFromNames** implementieren und Eigenschaftentags über die Ausgabe Parameter *LppPropTags* zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="661a1-125">If the message store provider wants to expose these named properties, it should implement **IMAPIProp::GetIDsFromNames** and return property tags through the output parameter  *lppPropTags*  .</span></span> <span data-ttu-id="661a1-126">Outlook kann mithilfe dieser Eigenschaftentags dann die [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) -Methode aufrufen, und der Nachricht Speicheranbieter den Kontonamen und Zeitstempel für das gewünschte Konto zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="661a1-126">Outlook can then call the [IMAPIProp::GetProps](http://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx) method by using these property tags, and the message store provider can return the account name and stamp of the desired account.</span></span> 
  
<span data-ttu-id="661a1-127">Zur Unterstützung der folgende benannten Eigenschaften erwarten Anbieter Outlook **IMAPIProp::GetIDsFromNames** verwendet, um das Eigenschafts-Tag für diese Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="661a1-127">To support these named properties, store providers should expect Outlook to use **IMAPIProp::GetIDsFromNames** to obtain the property tag for this property.</span></span> <span data-ttu-id="661a1-128">Outlook gibt die folgenden Werte für die [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) -Struktur, die dieser benannten Eigenschaft entspricht, die als Teil des Arrays an, der input-Parameter *LppPropNames* des **IMAPIProp::GetIDsFromNames**auf zeigt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="661a1-128">Outlook specifies the following values for the [MAPINAMEID](http://msdn.microsoft.com/library/9a92e9cd-8282-4cf0-93af-4089b3763594%28Office.15%29.aspx) structure that corresponds to this named property, which is passed as part of the array pointed at by the input parameter  *lppPropNames*  of **IMAPIProp::GetIDsFromNames**.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="661a1-129">x LpGuid:</span><span class="sxs-lookup"><span data-stu-id="661a1-129">lpGuid:</span></span>  <br/> |<span data-ttu-id="661a1-130">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="661a1-130">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="661a1-131">UlKind:</span><span class="sxs-lookup"><span data-stu-id="661a1-131">ulKind:</span></span>  <br/> |<span data-ttu-id="661a1-132">MNID_ID</span><span class="sxs-lookup"><span data-stu-id="661a1-132">MNID_ID</span></span>  <br/> |
|<span data-ttu-id="661a1-133">Kind.lID:</span><span class="sxs-lookup"><span data-stu-id="661a1-133">Kind.lID:</span></span>  <br/> |<span data-ttu-id="661a1-134">dispidInetAcctStamp</span><span class="sxs-lookup"><span data-stu-id="661a1-134">dispidInetAcctStamp</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="661a1-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="661a1-135">See also</span></span>

- [<span data-ttu-id="661a1-136">Über die Konto-API</span><span class="sxs-lookup"><span data-stu-id="661a1-136">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="661a1-137">Konstanten (Account Management API)</span><span class="sxs-lookup"><span data-stu-id="661a1-137">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="661a1-138">Kanonische PidLidInternetAccountStamp-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="661a1-138">PidLidInternetAccountStamp Canonical Property</span></span>](http://msdn.microsoft.com/library/819179fe-e58e-415c-abc7-1949036745ee%28Office.15%29.aspx)
