# terror
Proyecto de IA "Escribir para hablar" sobre una IA que cuente una historia de Terror

De:
- Christian Eduardo Navarro Curiel
- Landy Alberto Tolentino Olmedo

```python
import os
from groq import Groq

client = Groq()
speech_file_path = Path(__file__).parent / "speech.wav"
response = client.audio.speech.create(
  model="playai-tts",
  voice="Arista-PlayAI",
  response_format="wav",
  input="Here are three famous Mexican horror legends, each summarized in about 10 seconds:

---

**1. La Llorona (The Weeping Woman)**  
A vengeful spirit of a mother who drowned her children in a river after her lover betrayed her. Now, she wanders at night, wailing *"¡Ay, mis hijos!"* Her ghost lures people to the water to drown them. Ignoring her cries or approaching her means certain doom.  

---

**2. La Siguanaba (The Deceptive Hag)**  
An old woman with long hair who lures men into the forest. If you glimpse her face, it’s hideously distorted. Linked to the *Apeninos* (forest spirits), she’s often seen near rivers, warning that curiosity about her appearance brings terror.  

---

**3. El Sombrerón (The Wide-Hat Stranger)**  
A towering, shadowy figure in a wide-brimmed hat who stalks lonely roads. He demands travelers tell a story; if they fail, he steals their soul. Some say he’s a demon testing faith, others a guardian of secrets. Avoid his gaze and keep your stories sharp!  

--- 

Each legend blends tragedy, mystery, and a haunting moral lesson. ¡Cuidado!",
)
response.stream_to_file(speech_file_path)
```

```python
from groq import Groq

client = Groq()
completion = client.chat.completions.create(
    model="qwen-qwq-32b",
    messages=[
      {
        "role": "user",
        "content": "Tell me 3 famous Mexican horror legends, but I want those 3 Mexican horror legends to last 10 seconds each."
      },
      {
        "role": "assistant",
        "content": "\n<think>\nOkay, the user wants three famous Mexican horror legends, each summarized in about 10 seconds. Let me start by recalling some of the most well-known ones.\n\nFirst, La Llorona is definitely a top choice. The story of the weeping woman who drowns children. I should mention her backstory, the wailing, and the warning not to go near the river at night. Need to keep it concise but cover the key points.\n\nNext, El Chupacabra. Wait, is that Mexican? I think it's more associated with Puerto Rico and Latin America in general, but maybe it's considered Mexican too. Alternatively, maybe La Huilaca? Hmm, better double-check. Alternatively, the Cipactli or the Tlahuelpuchi. Wait, maybe I should stick with the most famous ones even if they're regional. Let me confirm El Chupacabra's origins. It's from Puerto Rico, but since the user asked for Mexican, maybe another legend. Maybe La Siguanaba? That's a Mexican legend. The old woman with a beautiful face when you look away. Yeah, that's a classic.\n\nThird option, maybe El Sombrerón? The tall, hat-wearing figure that appears to people, especially at night. Or the Apeninos, which are like the Mexican versions of the Jersey Devil? Or maybe La Llorona's a bit too common. Wait, I need three distinct ones. Let's see:\n\n1. La Llorona – definitely first.\n\n2. La Chonja – a witch who lures men to their death. Or La Viuda de Blancos? Wait, maybe La Ciguapa? No, that's Dominican. Hmm. Alternatively, the Cadejos, but they're more Guatemalan. Maybe the Tlahuelpuchi, which is a skeletal child. Or the Chupacabra if it's okay. Alternatively, the Tlahuelpuchi is a good one. Let me think of the most well-known ones. Maybe La Siguanaba is better because it's more well-known. The woman with the beautiful face, but when you look, she's hideous. That's a classic.\n\nWait, the user might know El Chupacabra, even if it's from Puerto Rico. Alternatively, maybe the most famous ones are La Llorona, El Sombrerón, and La Viuda de Blancos? Or La Chonja. Alternatively, the story of La Llorona, La Siguanaba, and El Chupacabra. I'll go with that, even if Chupacabra's origin is debated. Alternatively, maybe the Tlahuelpuchi. Let me structure each one with a quick backstory, the key elements, and the moral or warning. Each should be around 10 seconds, so about 1-2 sentences each. Let me check each:\n\nLa Llorona: Drowned her kids, now weeps at night, lures people to water. \n\nLa Siguanaba: Old woman with long hair, when you look at her face, it's grotesque. She's linked to the Apeninos.\n\nEl Chupacabra: Maybe okay, even if not strictly Mexican, it's widely recognized in the region. It's a creature that drains livestock, described as a reptilian being. \n\nAlternatively, maybe the Tlahuelpuchi, which is a skeletal child that leads people to their death. That's more Mexican. Let me confirm that Tlahuelpuchi is from Mexican folklore. Yes, from the Nahua people. \n\nAlternatively, La Viuda de Blancos – a vengeful spirit in white. Hmm. Maybe better to pick three that are definitely Mexican. Let me structure each entry with a quick summary, making sure each is distinct. \n\nAlternatively, the Cadejos are more from Guatemala, so maybe not. Let's go with:\n\n1. La Llorona\n\n2. La Siguanaba\n\n3. El Chupacabra (even if from Puerto Rico, it's well-known in Mexico too)\n\nAlternatively, the Apeninos, which are similar to Bigfoot, but maybe less known. Hmm. Alternatively, the Cihuateteo – women who died in childbirth becoming spirits. But maybe too obscure. \n\nAlternatively, La Chonja – a witch who turns into a dog to lure men. That's a good one. \n\nSo, perhaps:\n\n1. La Llorona\n\n2. La Chonja\n\n3. El Sombrerón\n\nAlternatively, La Viuda de Blancos. Hmm. Let me think of the top three. \n\nWait, let me check some sources. The most famous Mexican legends are La Llorona, El Chupacabra (though that's a modern legend), La Siguanaba, El Sombrerón, and La Chonja. \n\nAlternatively, the Tlahuelpuchi. Let me pick three that are most iconic. \n\nAlternatively, the story of La Llorona, La Chonja, and El Sombrerón. \n\nAlternatively, to ensure they are all from Mexico, I'll avoid Chupacabra. Let me go with:\n\n1. La Llorona\n\n2. La Chonja\n\n3. El Sombrerón\n\nAlternatively, La Viuda de Blancos. Let me structure each with a quick, concise explanation, focusing on origin, appearance, and the horror element. Each needs to be a brief 10-second summary. \n\nAlternatively, maybe the user might expect La Llorona, La Siguanaba, and El Chupacabra even if one is from Puerto Rico. But to be accurate, better to stick to Mexican ones. \n\nWait, La Siguanaba is definitely from Mexican folklore. El Sombrerón is as well. Let me confirm each:\n\n- La Llorona: Definitely Mexican.\n\n- La Siguanaba: Mexican, linked to the Apeninos.\n\n- El Sombrerón: Yes, a Mexican legend about a tall, shadowy figure.\n\nAlternatively, the Tlahuelpuchi: a skeletal child that lures people to their death. \n\nHmm, I think the user might know La Llorona and El Chupacabra, even if the latter is from Puerto Rico. But to be accurate, better to pick three that are authentically Mexican. \n\nSo, finalizing:\n\n1. La Llorona: Drowned her kids, now wails at night, lures to water.\n\n2. La Chonja: Witch who transforms into a dog, lures men to attack them.\n\n3. El Sombrerón: Tall, shadowy figure in wide-brimmed hat, haunts lonely roads.\n\nAlternatively, La Siguanaba: Old woman with long hair, hideous face when revealed, associated with the Apeninos. \n\nAlternatively, La Viuda de Blancos: A vengeful spirit in white who kills. \n\nI think La Chonja is a good second. Third could be El Chupacabra if acceptable, otherwise El Sombrerón. \n\nAlternatively, the most famous three are La Llorona, La Siguanaba, and El Sombrerón. \n\nOkay, let me outline each with a quick backstory, key features, and the horror aspect. Need to make sure each is under 10 seconds, so about 2-3 sentences each. \n\nWait, the user said \"legends\" so maybe include more traditional ones. Let me go with:\n\n1. La Llorona – the weeping woman, drowned kids, lures to drown others.\n\n2. La Siguanaba – old woman with long hair, hideous face when you look, linked to the Apeninos.\n\n3. El Sombrerón – tall, dark figure with a wide hat, haunts lonely men, demands a story, if you can't tell one, he takes your soul.\n\nAlternatively, the Tlahuelpuchi: skeletal child who leads to death.\n\nHmm, maybe better to go with the ones I listed. Let me check each for accuracy and conciseness.\n</think>\n\nHere are three famous Mexican horror legends, each summarized in about 10 seconds:\n\n---\n\n**1. La Llorona (The Weeping Woman)**  \nA vengeful spirit of a mother who drowned her children in a river after her lover betrayed her. Now, she wanders at night, wailing *\"¡Ay, mis hijos!\"* Her ghost lures people to the water to drown them. Ignoring her cries or approaching her means certain doom.  \n\n---\n\n**2. La Siguanaba (The Deceptive Hag)**  \nAn old woman with long hair who lures men into the forest. If you glimpse her face, it’s hideously distorted. Linked to the *Apeninos* (forest spirits), she’s often seen near rivers, warning that curiosity about her appearance brings terror.  \n\n---\n\n**3. El Sombrerón (The Wide-Hat Stranger)**  \nA towering, shadowy figure in a wide-brimmed hat who stalks lonely roads. He demands travelers tell a story; if they fail, he steals their soul. Some say he’s a demon testing faith, others a guardian of secrets. Avoid his gaze and keep your stories sharp!  \n\n--- \n\nEach legend blends tragedy, mystery, and a haunting moral lesson. ¡Cuidado!"
      },
      {
        "role": "user",
        "content": ""
      }
    ],
    temperature=0.6,
    max_completion_tokens=4096,
    top_p=0.95,
    stream=True,
    stop=None,
)

for chunk in completion:
    print(chunk.choices[0].delta.content or "", end="")
```

curl de la aplicacion con qwen-qwq-32b:

```shell
curl "https://api.groq.com/openai/v1/chat/completions" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer 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" \
  -d '{
         "messages": [
           {
             "role": "user",
             "content": "Tell me 3 famous Mexican horror legends, but I want those 3 Mexican horror legends to last 10 seconds each."
           },
           {
             "role": "assistant",
             "content": "\n<think>\nOkay, the user wants three famous Mexican horror legends, each summarized in about 10 seconds. Let me start by recalling some of the most well-known ones.\n\nFirst, La Llorona is definitely a top choice. The story of the weeping woman who drowns children. I should mention her backstory, the wailing, and the warning not to go near the river at night. Need to keep it concise but cover the key points.\n\nNext, El Chupacabra. Wait, is that Mexican? I think it'\''s more associated with Puerto Rico and Latin America in general, but maybe it'\''s considered Mexican too. Alternatively, maybe La Huilaca? Hmm, better double-check. Alternatively, the Cipactli or the Tlahuelpuchi. Wait, maybe I should stick with the most famous ones even if they'\''re regional. Let me confirm El Chupacabra'\''s origins. It'\''s from Puerto Rico, but since the user asked for Mexican, maybe another legend. Maybe La Siguanaba? That'\''s a Mexican legend. The old woman with a beautiful face when you look away. Yeah, that'\''s a classic.\n\nThird option, maybe El Sombrerón? The tall, hat-wearing figure that appears to people, especially at night. Or the Apeninos, which are like the Mexican versions of the Jersey Devil? Or maybe La Llorona'\''s a bit too common. Wait, I need three distinct ones. Let'\''s see:\n\n1. La Llorona – definitely first.\n\n2. La Chonja – a witch who lures men to their death. Or La Viuda de Blancos? Wait, maybe La Ciguapa? No, that'\''s Dominican. Hmm. Alternatively, the Cadejos, but they'\''re more Guatemalan. Maybe the Tlahuelpuchi, which is a skeletal child. Or the Chupacabra if it'\''s okay. Alternatively, the Tlahuelpuchi is a good one. Let me think of the most well-known ones. Maybe La Siguanaba is better because it'\''s more well-known. The woman with the beautiful face, but when you look, she'\''s hideous. That'\''s a classic.\n\nWait, the user might know El Chupacabra, even if it'\''s from Puerto Rico. Alternatively, maybe the most famous ones are La Llorona, El Sombrerón, and La Viuda de Blancos? Or La Chonja. Alternatively, the story of La Llorona, La Siguanaba, and El Chupacabra. I'\''ll go with that, even if Chupacabra'\''s origin is debated. Alternatively, maybe the Tlahuelpuchi. Let me structure each one with a quick backstory, the key elements, and the moral or warning. Each should be around 10 seconds, so about 1-2 sentences each. Let me check each:\n\nLa Llorona: Drowned her kids, now weeps at night, lures people to water. \n\nLa Siguanaba: Old woman with long hair, when you look at her face, it'\''s grotesque. She'\''s linked to the Apeninos.\n\nEl Chupacabra: Maybe okay, even if not strictly Mexican, it'\''s widely recognized in the region. It'\''s a creature that drains livestock, described as a reptilian being. \n\nAlternatively, maybe the Tlahuelpuchi, which is a skeletal child that leads people to their death. That'\''s more Mexican. Let me confirm that Tlahuelpuchi is from Mexican folklore. Yes, from the Nahua people. \n\nAlternatively, La Viuda de Blancos – a vengeful spirit in white. Hmm. Maybe better to pick three that are definitely Mexican. Let me structure each entry with a quick summary, making sure each is distinct. \n\nAlternatively, the Cadejos are more from Guatemala, so maybe not. Let'\''s go with:\n\n1. La Llorona\n\n2. La Siguanaba\n\n3. El Chupacabra (even if from Puerto Rico, it'\''s well-known in Mexico too)\n\nAlternatively, the Apeninos, which are similar to Bigfoot, but maybe less known. Hmm. Alternatively, the Cihuateteo – women who died in childbirth becoming spirits. But maybe too obscure. \n\nAlternatively, La Chonja – a witch who turns into a dog to lure men. That'\''s a good one. \n\nSo, perhaps:\n\n1. La Llorona\n\n2. La Chonja\n\n3. El Sombrerón\n\nAlternatively, La Viuda de Blancos. Hmm. Let me think of the top three. \n\nWait, let me check some sources. The most famous Mexican legends are La Llorona, El Chupacabra (though that'\''s a modern legend), La Siguanaba, El Sombrerón, and La Chonja. \n\nAlternatively, the Tlahuelpuchi. Let me pick three that are most iconic. \n\nAlternatively, the story of La Llorona, La Chonja, and El Sombrerón. \n\nAlternatively, to ensure they are all from Mexico, I'\''ll avoid Chupacabra. Let me go with:\n\n1. La Llorona\n\n2. La Chonja\n\n3. El Sombrerón\n\nAlternatively, La Viuda de Blancos. Let me structure each with a quick, concise explanation, focusing on origin, appearance, and the horror element. Each needs to be a brief 10-second summary. \n\nAlternatively, maybe the user might expect La Llorona, La Siguanaba, and El Chupacabra even if one is from Puerto Rico. But to be accurate, better to stick to Mexican ones. \n\nWait, La Siguanaba is definitely from Mexican folklore. El Sombrerón is as well. Let me confirm each:\n\n- La Llorona: Definitely Mexican.\n\n- La Siguanaba: Mexican, linked to the Apeninos.\n\n- El Sombrerón: Yes, a Mexican legend about a tall, shadowy figure.\n\nAlternatively, the Tlahuelpuchi: a skeletal child that lures people to their death. \n\nHmm, I think the user might know La Llorona and El Chupacabra, even if the latter is from Puerto Rico. But to be accurate, better to pick three that are authentically Mexican. \n\nSo, finalizing:\n\n1. La Llorona: Drowned her kids, now wails at night, lures to water.\n\n2. La Chonja: Witch who transforms into a dog, lures men to attack them.\n\n3. El Sombrerón: Tall, shadowy figure in wide-brimmed hat, haunts lonely roads.\n\nAlternatively, La Siguanaba: Old woman with long hair, hideous face when revealed, associated with the Apeninos. \n\nAlternatively, La Viuda de Blancos: A vengeful spirit in white who kills. \n\nI think La Chonja is a good second. Third could be El Chupacabra if acceptable, otherwise El Sombrerón. \n\nAlternatively, the most famous three are La Llorona, La Siguanaba, and El Sombrerón. \n\nOkay, let me outline each with a quick backstory, key features, and the horror aspect. Need to make sure each is under 10 seconds, so about 2-3 sentences each. \n\nWait, the user said \"legends\" so maybe include more traditional ones. Let me go with:\n\n1. La Llorona – the weeping woman, drowned kids, lures to drown others.\n\n2. La Siguanaba – old woman with long hair, hideous face when you look, linked to the Apeninos.\n\n3. El Sombrerón – tall, dark figure with a wide hat, haunts lonely men, demands a story, if you can'\''t tell one, he takes your soul.\n\nAlternatively, the Tlahuelpuchi: skeletal child who leads to death.\n\nHmm, maybe better to go with the ones I listed. Let me check each for accuracy and conciseness.\n</think>\n\nHere are three famous Mexican horror legends, each summarized in about 10 seconds:\n\n---\n\n**1. La Llorona (The Weeping Woman)**  \nA vengeful spirit of a mother who drowned her children in a river after her lover betrayed her. Now, she wanders at night, wailing *\"¡Ay, mis hijos!\"* Her ghost lures people to the water to drown them. Ignoring her cries or approaching her means certain doom.  \n\n---\n\n**2. La Siguanaba (The Deceptive Hag)**  \nAn old woman with long hair who lures men into the forest. If you glimpse her face, it’s hideously distorted. Linked to the *Apeninos* (forest spirits), she’s often seen near rivers, warning that curiosity about her appearance brings terror.  \n\n---\n\n**3. El Sombrerón (The Wide-Hat Stranger)**  \nA towering, shadowy figure in a wide-brimmed hat who stalks lonely roads. He demands travelers tell a story; if they fail, he steals their soul. Some say he’s a demon testing faith, others a guardian of secrets. Avoid his gaze and keep your stories sharp!  \n\n--- \n\nEach legend blends tragedy, mystery, and a haunting moral lesson. ¡Cuidado!"
           },
           {
             "role": "user",
             "content": ""
           }
         ],
         "model": "qwen-qwq-32b",
         "temperature": 0.6,
         "max_completion_tokens": 4096,
         "top_p": 0.95,
         "stream": false,
         "stop": null
       }'
```

curl de la aplicacion con

```shell
curl -X POST "https://api.groq.com/openai/v1/audio/speech" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer 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" \
  -d '{
         "model": "playai-tts",
         "voice": "Arista-PlayAI",
         "input": "Here are three famous Mexican horror legends, each summarized in about 10 seconds:\n\n---\n\n**1. La Llorona (The Weeping Woman)**  \nA vengeful spirit of a mother who drowned her children in a river after her lover betrayed her. Now, she wanders at night, wailing *\"¡Ay, mis hijos!\"* Her ghost lures people to the water to drown them. Ignoring her cries or approaching her means certain doom.  \n\n---\n\n**2. La Siguanaba (The Deceptive Hag)**  \nAn old woman with long hair who lures men into the forest. If you glimpse her face, it’s hideously distorted. Linked to the *Apeninos* (forest spirits), she’s often seen near rivers, warning that curiosity about her appearance brings terror.  \n\n---\n\n**3. El Sombrerón (The Wide-Hat Stranger)**  \nA towering, shadowy figure in a wide-brimmed hat who stalks lonely roads. He demands travelers tell a story; if they fail, he steals their soul. Some say he’s a demon testing faith, others a guardian of secrets. Avoid his gaze and keep your stories sharp!  \n\n--- \n\nEach legend blends tragedy, mystery, and a haunting moral lesson. ¡Cuidado!",
         "response_format": "wav"
       }' \
  --output out.wav
```