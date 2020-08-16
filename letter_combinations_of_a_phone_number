class Solution:
    def letterCombinations(self, digits: str) -> List[str]:
        keymap = {
            1 : [],
            2 : ["a", "b", "c"],
            3 : ["d", "e", "f"],
            4 : ["g", "h", "i"],
            5 : ["j", "k", "l"],
            6 : ["m", "n", "o"],
            7 : ["p", "q", "r", "s"],
            8 : ["t", "u", "v"],
            9 : ["w", "x", "y", "z"],
            0 : [" "]
        }
        
        words = []
        
        for key in digits:
            key = int(key)
            pos_chars = keymap[key]
        
            if (len(words) == 0):
                words = pos_chars
                continue
        
            newWords = []
        
            for word in words:
                for char in pos_chars:
                    newWord = word + char
                    newWords.append(newWord)
        
            words = newWords
        
        return words
        
    
    
