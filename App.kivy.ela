from kivy.app import App
from kivy.uix.boxlayout import BoxLayout
from kivy.uix.scrollview import ScrollView
from kivy.uix.label import Label
from kivy.uix.textinput import TextInput
from kivy.uix.button import Button
from kivy.uix.popup import Popup
from kivy.core.window import Window
from kivy.metrics import dp
import random

# قوائم النصائح (بالفرنسية)
study_tips = [
    "Utilisez la technique Pomodoro: 25 minutes d'étude et 5 minutes de pause - cette technique vous aidera à maintenir votre motivation",
    "Aménagez un environnement d'étude organisé comme un bureau ou une bibliothèque publique - évitez d'étudier sur le lit",
    "Étudiez la leçon trois fois: avant le cours, pendant le cours et après le cours",
    "Concentrez-vous sur tout ce que l'enseignant dira et consacrez un cahier à la prise de notes",
    "Regardez des vidéos 'Study With Me' sur YouTube pour vous motiver à étudier",
    "Achetez des livres de révision pour la maison car ils vous aideront beaucoup pour les révisions",
    "Utilisez des résumés et des diagrammes pour mémoriser",
    "Ne mémorisez pas seulement l'information mais comprenez-la bien avant de la mémoriser",
    "Suivez de nombreuses chaînes YouTube car elles vous aideront à simplifier les informations",
    "Utilisez un surligneur pour marquer les informations importantes",
    "Expliquez l'information à une autre personne même absente comme si vous étiez l'enseignant",
    "La planification et la gestion du temps sont la base de l'excellence - établissez des plans stricts pour chaque semaine",
    "Un sommeil suffisant de 7 à 9 heures est plus important qu'une heure supplémentaire d'étude"
]

glowup_tips = [
    "Buvez 6 à 8 verres d'eau par jour pour hydrater le corps",
    "Faites 5 minutes d'exercices simples par jour",
    "Utilisez l'huile d'olive comme hydratant naturel pour la peau",
    "Utilisez un nettoyant visage adapté à votre type de peau",
    "Massez votre visage avec des glaçons quotidiennement",
    "Exposez votre visage à la vapeur pour ouvrir les pores",
    "Utilisez l'eau de girofle comme tonique naturel",
    "Appliquez un masque au concombre pour le visage",
    "Utilisez un masque à la tomate pour le visage",
    "Appliquez un masque à la levure de boulanger avec de l'eau sur le visage",
    "Utilisez de l'huile d'olive, du café et du sucre pour exfolier la peau",
    "Utilisez de l'huile d'olive, du sucre et du citron pour exfolier les lèvres",
    "Utilisez de l'huile d'olive et du sucre pour exfolier le corps",
    "Appliquez un baume à lèvres quotidiennement",
    "Faites un massage facial quotidien pour raffermir la peau",
    "Lavez la zone intime avec de l'eau seulement",
    "Prenez une douche quotidiennement",
    "Appliquez du déodorant et du parfum deux fois par jour",
    "Appliquez un masque à l'huile d'olive sur les cheveux 30 minutes avant la douche et massez le cuir chevelu",
    "Lavez seulement le cuir chevelu",
    "Appliquez un masque au riz sur les cheveux",
    "Ne brossez pas les cheveux mouillés",
    "Mangez une alimentation saine",
    "Pratiquez la prière, lisez le Coran et les invocations du matin",
    "Dormez suffisamment",
    "Évitez les écrans avant de dormir et au réveil",
    "Utilisez un cahier pour écrire ce que vous pensez afin de réduire le stress",
    "Fixez des objectifs à respecter",
    "Évitez de vous comparer aux autres",
    "Dites toujours au réveil: Je suis prêt(e) à commencer une nouvelle journée de ma vie"
]

routines = [
    "Routine matinale: Réveil tôt à 7h00 en veillant à avoir suffisamment de sommeil - Boire un verre d'eau en méditant à la fenêtre et écrire les tâches de la journée - Faire 5 minutes d'exercice - Prendre une douche - Suivre la routine quotidienne pour les cheveux, le corps et la peau - Prendre un petit-déjeuner sain puis commencer les tâches",
    "Routine du soir: Après avoir terminé toutes les tâches, commencez la routine du soir - Suivez la routine de soins de la peau - Portez des vêtements confortables - Allez dîner - Préparez une tisane pour réduire le stress et vous calmer tout en lisant un livre - Regardez un film ou une série - Préparez-vous à dormir"
]

free_time_tips = [
    "Dessin: Dessinez des œuvres à accrocher au mur de votre chambre",
    "Faites des travaux manuels avec du papier blanc comme des boîtes, des pots à crayons ou même des porte-stylos",
    "Cuisine: Aidez votre mère dans les tâches ménagères",
    "Regardez un documentaire",
    "Lisez des livres",
    "Apprenez une nouvelle compétence",
    "Jouez avec des amis",
    "Téléchargez des jeux sur votre téléphone et jouez pour vous amuser",
    "Pratiquez un sport",
    "Prenez un long bain chaud"
]

recipes = [
    "Recette d'œufs aux légumes: œufs + tomates + oignon + poivron + huile d'olive",
    "Recette de flocons d'avoine au lait: avoine + lait + miel + banane + noix",
    "Recette de salade healthy: laitue + concombre + tomate + carotte + huile d'olive + citron",
    "Recette de smoothie: banane + lait + miel + avoine + glace"
]

# القاموس الرئيسي (الكلمات المفتاحية بالفرنسية)
keywords = {
    # الدراسة
    "étude": study_tips,
    "étudier": study_tips,
    "devoirs": study_tips, 
    "examen": study_tips,
    "révision": study_tips,
    "école": study_tips,
    "conseils étude": study_tips,
    
    # العناية
    "beauté": glowup_tips,
    "soins": glowup_tips,
    "peau": glowup_tips,
    "cheveux": glowup_tips,
    "conseils beauté": glowup_tips,
    "glowup": glowup_tips,
    
    # الروتين
    "routine": routines,
    "matin": routines,
    "soir": routines,
    
    # وقت الفراغ
    "loisirs": free_time_tips,
    "temps libre": free_time_tips,
    "divertissement": free_time_tips,
    "activités": free_time_tips,
    
    # وصفات
    "recette": recipes,
    "nourriture": recipes,
    "manger": recipes,
    "cuisine": recipes,
    "repas": recipes,
    
    # تحيات
    "bonjour": ["Bonjour ! Comment puis-je vous aider aujourd'hui ?"],
    "salut": ["Salut ! Je suis le bot d'aide intelligent"],
    "hello": ["Hello ! Je suis le bot d'aide intelligent"],
    
    # اسم
    "nom": ["Ravi de vous rencontrer ! Je serai heureux de vous aider"],
    
    # شكر
    "merci": ["De rien ! Je suis toujours là pour vous aider", "Avec plaisir ! Continuez vos progrès"],
    "thanks": ["De rien ! Je suis toujours là pour vous aider"]
}

class ChatLabel(Label):
    """تخصيص Label لعرض الرسائل بشكل أفضل"""
    pass

class ChatBotApp(BoxLayout):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)
        self.orientation = 'vertical'
        self.padding = dp(10)
        self.spacing = dp(10)
        
        # تعيين لون الخلفية
        Window.clearcolor = (0.94, 0.97, 1, 1)  # #f0f8ff
        
        self.create_widgets()
        
    def create_widgets(self):
        # عنوان التطبيق
        title_label = Label(
            text="Bot d'Aide Intelligent 🤖",
            font_size='20sp',
            bold=True,
            size_hint_y=None,
            height=dp(40),
            color=(0.17, 0.24, 0.31, 1)  # #2c3e50
        )
        self.add_widget(title_label)
        
        # إطار الأزرار
        button_layout = BoxLayout(
            size_hint_y=None,
            height=dp(40),
            spacing=dp(5)
        )
        
        help_button = Button(
            text="Aide",
            background_color=(0.20, 0.60, 0.86, 1),  # #3498db
            on_press=self.show_help
        )
        
        clear_button = Button(
            text="Effacer",
            background_color=(0.91, 0.30, 0.24, 1),  # #e74c3c
            on_press=self.clear_chat
        )
        
        button_layout.add_widget(help_button)
        button_layout.add_widget(clear_button)
        self.add_widget(button_layout)
        
        # منطقة الدردشة مع ScrollView
        self.chat_scroll = ScrollView()
        self.chat_layout = BoxLayout(
            orientation='vertical',
            size_hint_y=None,
            spacing=dp(5),
            padding=dp(10)
        )
        self.chat_layout.bind(minimum_height=self.chat_layout.setter('height'))
        
        self.chat_scroll.add_widget(self.chat_layout)
        self.add_widget(self.chat_scroll)
        
        # رسالة الترحيب
        self.add_message("Bot d'Aide Intelligent 🤖", is_bot=True)
        self.add_message("Je peux vous aider avec: études, beauté, recettes, routines, loisirs", is_bot=True)
        self.add_message("Posez-moi une question et appuyez sur Envoyer", is_bot=True)
        
        # إطار الإدخال
        input_layout = BoxLayout(
            size_hint_y=None,
            height=dp(50),
            spacing=dp(5)
        )
        
        self.user_input = TextInput(
            hint_text="Tapez votre message ici...",
            multiline=False,
            size_hint_x=0.7
        )
        self.user_input.bind(on_text_validate=self.get_response)
        
        send_button = Button(
            text="Envoyer",
            size_hint_x=0.3,
            background_color=(0.20, 0.60, 0.86, 1),  # #3498db
            on_press=self.get_response
        )
        
        input_layout.add_widget(self.user_input)
        input_layout.add_widget(send_button)
        self.add_widget(input_layout)
        
        # توجيهات الاستخدام
        guide_label = Label(
            text="Posez vos questions en français",
            font_size='12sp',
            italic=True,
            size_hint_y=None,
            height=dp(30),
            color=(0.50, 0.55, 0.55, 1)  # #7f8c8d
        )
        self.add_widget(guide_label)
    
    def add_message(self, message, is_bot=False):
        """إضافة رسالة إلى منطقة الدردشة"""
        prefix = "Bot: " if is_bot else "Vous: "
        message_label = Label(
            text=f"{prefix}{message}",
            text_size=(Window.width - dp(40), None),
            size_hint_y=None,
            height=self.calculate_text_height(message),
            halign='left',
            valign='top'
        )
        message_label.bind(size=message_label.setter('text_size'))
        
        # تخصيص الألوان
        if is_bot:
            message_label.color = (0.17, 0.24, 0.31, 1)  # #2c3e50 (أزرق غامق)
        else:
            message_label.color = (0.09, 0.63, 0.52, 1)  # #16a085 (أخضر)
        
        self.chat_layout.add_widget(message_label)
        
        # التمرير إلى الأسفل
        self.chat_scroll.scroll_to(message_label)
    
    def calculate_text_height(self, text):
        """حساب الارتفاع المطلوب للنص"""
        line_height = dp(20)
        max_width = Window.width - dp(40)
        words = text.split()
        lines = []
        current_line = []
        
        for word in words:
            test_line = ' '.join(current_line + [word])
            test_label = Label(text=test_line)
            test_label.text_size = (max_width, None)
            test_label.texture_update()
            
            if test_label.texture_size[0] <= max_width:
                current_line.append(word)
            else:
                lines.append(' '.join(current_line))
                current_line = [word]
        
        if current_line:
            lines.append(' '.join(current_line))
        
        return max(len(lines) * line_height, dp(30))
    
    def get_response(self, instance):
        """معالجة رسالة المستخدم وإرسال الرد"""
        user_input = self.user_input.text.strip()
        if not user_input:
            return
        
        # إضافة رسالة المستخدم
        self.add_message(user_input, is_bot=False)
        
        response = ""
        user_input_lower = user_input.lower()
        
        # البحث عن كلمة مفتاحية في المدخلات
        found = False
        for keyword, tips in keywords.items():
            if keyword in user_input_lower:
                response = random.choice(tips)
                found = True
                break
        
        # إذا لم يتم العثور على كلمة مفتاحية
        if not found:
            if any(word in user_input_lower for word in ["bonjour", "salut", "hello", "coucou"]):
                response = random.choice(keywords["bonjour"])
            elif any(word in user_input_lower for word in ["merci", "remercie", "thanks"]):
                response = random.choice(keywords["merci"])
            else:
                response = "Désolé, je n'ai pas compris votre question. Vous pouvez poser des questions sur: études, beauté, routines, loisirs ou recettes."
        
        # إضافة رد البوت
        self.add_message(response, is_bot=True)
        
        # مسح حقل الإدخال
        self.user_input.text = ""
    
    def show_help(self, instance):
        """عرض نافذة المساعدة"""
        help_text = """Comment puis-je vous aider?
- Conseils d'étude (étude, devoirs, examen, révision)
- Conseils beauté (beauté, soins, peau, cheveux)
- Routines (routine, matin, soir)
- Activités de loisirs (loisirs, temps libre, divertissement)
- Recettes (recette, nourriture, cuisine)

Exemples de questions:
- "Des conseils pour étudier ?"
- "Comment prendre soin de ma peau ?"
- "Quelle routine matinale ?"
- "Que faire pendant mon temps libre ?"
- "Une recette healthy ?"
"""
        
        popup_layout = BoxLayout(orientation='vertical', padding=dp(10), spacing=dp(10))
        help_label = Label(
            text=help_text,
            text_size=(Window.width * 0.8, None),
            size_hint_y=None,
            height=self.calculate_text_height(help_text) + dp(50)
        )
        help_label.bind(size=help_label.setter('text_size'))
        
        close_button = Button(
            text="Fermer",
            size_hint_y=None,
            height=dp(40)
        )
        
        popup_layout.add_widget(help_label)
        popup_layout.add_widget(close_button)
        
        popup = Popup(
            title='Aide',
            content=popup_layout,
            size_hint=(0.9, 0.8)
        )
        
        close_button.bind(on_press=popup.dismiss)
        popup.open()
    
    def clear_chat(self, instance):
        """مسح المحادثة"""
        self.chat_layout.clear_widgets()
        self.add_message("Bot d'Aide Intelligent 🤖", is_bot=True)
        self.add_message("Je peux vous aider avec: études, beauté, recettes, routines, loisirs", is_bot=True)
        self.add_message("Posez-moi une question et appuyez sur Envoyer", is_bot=True)

class IntelligentHelpBotApp(App):
    def build(self):
        self.title = "Bot d'Aide Intelligent"
        return ChatBotApp()

if __name__ == '__main__':
    IntelligentHelpBotApp().run()
